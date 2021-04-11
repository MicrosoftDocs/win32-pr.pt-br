---
description: Descreve os códigos de erro 500-999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Códigos de erro do sistema (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164102"
---
# <a name="system-error-codes-500-999"></a>Códigos de erro do sistema (500-999)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) (erros 500 a 999). Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERRO \_ ao \_ carregar perfil do usuário \_**
</dt> <dd> <dl> <dt>

500 (0x1F4)
</dt> <dt>



Não é possível carregar o perfil do usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_estouro aritmético de erro \_**
</dt> <dd> <dl> <dt>

534 (0x216)
</dt> <dt>



O resultado aritmético excedeu 32 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**PIPE de erro \_ \_ conectado**
</dt> <dd> <dl> <dt>

535 (0x217)
</dt> <dt>



Há um processo em outra extremidade do pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**\_escuta de pipe de erro \_**
</dt> <dd> <dl> <dt>

536 (0x218)
</dt> <dt>



Aguardando um processo abrir a outra extremidade do pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**\_interrupção do verificador de erro \_**
</dt> <dd> <dl> <dt>

537 (0x219)
</dt> <dt>



O verificador de aplicativo encontrou um erro no processo atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**erro \_ ABIOS \_**
</dt> <dd> <dl> <dt>

538 (0x21A)
</dt> <dt>



Ocorreu um erro no subsistema ABIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**\_Aviso de WX86 de erro \_**
</dt> <dd> <dl> <dt>

539 (0x21B)
</dt> <dt>



Ocorreu um aviso no subsistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Erro \_ WX86 \_**
</dt> <dd> <dl> <dt>

540 (0x21C)
</dt> <dt>



Ocorreu um erro no subsistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_temporizador de erro \_ não \_ cancelado**
</dt> <dd> <dl> <dt>

541 (0x21D)
</dt> <dt>



Foi feita uma tentativa de cancelar ou definir um temporizador que tem uma APC associada e o thread do assunto não é o thread que originalmente definiu o temporizador com uma rotina APC associada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**\_desenrolar erro**
</dt> <dd> <dl> <dt>

542 (0x21E)
</dt> <dt>



Desenrolar código de exceção.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERRO \_ de \_ pilha inadequada**
</dt> <dd> <dl> <dt>

543 (0x21F)
</dt> <dt>



Uma pilha inválida ou não alinhada foi encontrada durante uma operação de desenrolamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**\_destino de \_ liberação \_ inválido de erro**
</dt> <dd> <dl> <dt>

544 (0x220)
</dt> <dt>



Um destino de desenrolamento inválido foi encontrado durante uma operação de desenrolamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERRO \_ de \_ atributos de porta inválidos \_**
</dt> <dd> <dl> <dt>

545 (0x221)
</dt> <dt>



Atributos de objeto inválidos especificados para NtCreatePort ou atributos de porta inválidos especificados para NtConnectPort


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**mensagem de porta de erro \_ \_ \_ muito \_ longa**
</dt> <dd> <dl> <dt>

546 (0x222)
</dt> <dt>



O comprimento da mensagem passado para NtRequestPort ou NtRequestWaitReplyPort foi maior do que a mensagem máxima permitida pela porta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERRO \_ de \_ cota inválida \_ inferior**
</dt> <dd> <dl> <dt>

547 (0x223)
</dt> <dt>



Foi feita uma tentativa de reduzir um limite de cota abaixo do uso atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**dispositivo de erro \_ \_ já \_ anexado**
</dt> <dd> <dl> <dt>

548 (0x224)
</dt> <dt>



Foi feita uma tentativa de anexar a um dispositivo que já estava anexado a outro dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**inalinhamento de instrução de erro \_ \_**
</dt> <dd> <dl> <dt>

549 (0x225)
</dt> <dt>



Foi feita uma tentativa de executar uma instrução em um endereço não alinhado e o sistema host não oferece suporte a referências de instruções não alinhadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**criação de perfil de erro \_ \_ não \_ iniciada**
</dt> <dd> <dl> <dt>

550 (0x226)
</dt> <dt>



A criação de perfil não foi iniciada.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**criação de perfil de erro \_ \_ não \_ parada**
</dt> <dd> <dl> <dt>

551 (0x227)
</dt> <dt>



A criação de perfil não foi interrompida.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERRO \_ não foi possível \_ \_ interpretar**
</dt> <dd> <dl> <dt>

552 (0x228)
</dt> <dt>



A ACL passada não continha as informações mínimas necessárias.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**\_criação de perfil \_ de erro em \_ limite**
</dt> <dd> <dl> <dt>

553 (0x229)
</dt> <dt>



O número de objetos de criação de perfil ativos está no máximo e não é mais possível iniciá-lo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERRO não é possível \_ \_ aguardar**
</dt> <dd> <dl> <dt>

554 (0x22A)
</dt> <dt>



Usado para indicar que uma operação não pode continuar sem bloqueio de e/s.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERRO não é possível \_ \_ encerrar \_ automaticamente**
</dt> <dd> <dl> <dt>

555 (0x22B)
</dt> <dt>



Indica que um thread tentou se encerrar por padrão (chamado NtTerminateThread com **NULL**) e foi o último thread no processo atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERRO \_ inesperado ao \_ criar erro mm \_ \_**
</dt> <dd> <dl> <dt>

556 (0x22C)
</dt> <dt>



Se um erro MM for retornado, o que não está definido no filtro FsRtl padrão, ele será convertido em um dos seguintes erros que tem a garantia de estar no filtro. No entanto, nesse caso, as informações são perdidas, mas o filtro manipula corretamente a exceção.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**erro erro de \_ \_ \_ mapeamento \_ mm inesperado**
</dt> <dd> <dl> <dt>

557 (0x22D)
</dt> <dt>



Se um erro MM for retornado, o que não está definido no filtro FsRtl padrão, ele será convertido em um dos seguintes erros que tem a garantia de estar no filtro. No entanto, nesse caso, as informações são perdidas, mas o filtro manipula corretamente a exceção.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERRO \_ inesperado ao \_ \_ estender \_ Err**
</dt> <dd> <dl> <dt>

558 (0x22E)
</dt> <dt>



Se um erro MM for retornado, o que não está definido no filtro FsRtl padrão, ele será convertido em um dos seguintes erros que tem a garantia de estar no filtro. No entanto, nesse caso, as informações são perdidas, mas o filtro manipula corretamente a exceção.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERRO \_ de \_ tabela de função inadequada \_**
</dt> <dd> <dl> <dt>

559 (0x22F)
</dt> <dt>



Uma tabela de funções malformada foi encontrada durante uma operação de desenrolamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERRO \_ sem \_ tradução de GUID \_**
</dt> <dd> <dl> <dt>

560 (0x230)
</dt> <dt>



Indica que foi feita uma tentativa de atribuir proteção a um arquivo do sistema de arquivos ou diretório, e um dos SIDs no descritor de segurança não pôde ser convertido em um GUID que pudesse ser armazenado pelo sistema de arquivos. Isso faz com que a tentativa de proteção falhe, o que pode causar uma falha na tentativa de criação de arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERRO \_ de \_ tamanho inválido de LDT \_**
</dt> <dd> <dl> <dt>

561 (0x231)
</dt> <dt>



Indica que foi feita uma tentativa de aumentar um LDT definindo seu tamanho ou que o tamanho não era um número par de seletores.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERRO \_ de \_ deslocamento de LDT inválido \_**
</dt> <dd> <dl> <dt>

563 (0x233)
</dt> <dt>



Indica que o valor inicial para as informações de LDT não era um múltiplo integral do tamanho do seletor.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERRO \_ \_ descritor de LDT inválido \_**
</dt> <dd> <dl> <dt>

564 (0x234)
</dt> <dt>



Indica que o usuário forneceu um descritor inválido ao tentar configurar os descritores do LDT.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERRO \_ de \_ muitos \_ threads**
</dt> <dd> <dl> <dt>

565 (0x235)
</dt> <dt>



Indica que um processo tem muitos threads para executar a ação solicitada. Por exemplo, a atribuição de um token primário só pode ser executada quando um processo tem zero ou um thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_thread \_ de erro não está \_ em \_ processo**
</dt> <dd> <dl> <dt>

566 (0x236)
</dt> <dt>



Foi feita uma tentativa de operar em um thread dentro de um processo específico, mas o thread especificado não está no processo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**\_cota de arquivo de paginação de erro \_ \_ excedida**
</dt> <dd> <dl> <dt>

567 (0x237)
</dt> <dt>



A cota do arquivo de paginação foi excedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**\_ \_ conflito do servidor de logon de erro \_**
</dt> <dd> <dl> <dt>

568 (0x238)
</dt> <dt>



O serviço Netlogon não pode ser iniciado porque outro serviço Netlogon em execução no domínio está em conflito com a função especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**sincronização de erro \_ \_ necessária**
</dt> <dd> <dl> <dt>

569 (0x239)
</dt> <dt>



O banco de dados SAM em um Windows Server é significativamente fora de sincronização com a cópia no controlador de domínio. Uma sincronização completa é necessária.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERRO \_ net \_ Open \_ falhou**
</dt> <dd> <dl> <dt>

570 (0x23A)
</dt> <dt>



Falha na API NtCreateFile. Esse erro nunca deve ser retornado a um aplicativo, é um espaço reservado para o redirecionador do Gerenciador de LAN do Windows usar em suas rotinas de mapeamento de erros internas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**\_ \_ falha no privilégio de es de erro \_**
</dt> <dd> <dl> <dt>

571 (0x23B)
</dt> <dt>



{Falha no privilégio} Não foi possível alterar as permissões de e/s do processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**sair do controle de erro \_ \_ C \_**
</dt> <dd> <dl> <dt>

572 (0x23C)
</dt> <dt>



{Saída do aplicativo por CTRL + C} O aplicativo foi encerrado como resultado de um CTRL + C.


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERRO \_ de \_ systemfile ausente**
</dt> <dd> <dl> <dt>

573 (0x23D)
</dt> <dt>



{Arquivo de sistema ausente} O arquivo de sistema necessário% HS está insatisfatório ou ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERRO de \_ exceção sem tratamento \_**
</dt> <dd> <dl> <dt>

574 (0x23E)
</dt> <dt>



{Erro de aplicativo} A exceção% s (0x% 08lx) ocorreu no aplicativo no local 0x% 08lx.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**\_ \_ falha na inicialização do aplicativo de erro \_**
</dt> <dd> <dl> <dt>

575 (0x23F)
</dt> <dt>



{Erro de aplicativo} O aplicativo não pôde ser iniciado corretamente (0x% lx). Clique em OK para fechar o aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERRO \_ \_ ao criar arquivo de paginação \_**
</dt> <dd> <dl> <dt>

576 (0x240)
</dt> <dt>



{Não é possível criar arquivo de paginação} Falha na criação do arquivo de paginação% HS (% LX). O tamanho solicitado era% ld.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERRO \_ de \_ hash de imagem inválido \_**
</dt> <dd> <dl> <dt>

577 (0x241)
</dt> <dt>



O Windows não pode verificar a assinatura digital deste arquivo. Uma alteração recente de hardware ou software pode ter instalado um arquivo que está assinado incorretamente ou danificado ou que pode ser um software mal-intencionado de uma fonte desconhecida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERRO \_ sem \_ arquivo de paginação**
</dt> <dd> <dl> <dt>

578 (0x242)
</dt> <dt>



{Nenhum arquivo de paginação especificado} Nenhum arquivo de paginação foi especificado na configuração do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERRO \_ de \_ contexto flutuante inválido \_**
</dt> <dd> <dl> <dt>

579 (0x243)
</dt> <dt>



Exception Um aplicativo de modo real emitiu uma instrução de ponto flutuante e um hardware de ponto flutuante não está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERRO \_ nenhum \_ par de eventos \_**
</dt> <dd> <dl> <dt>

580 (0x244)
</dt> <dt>



Uma operação de sincronização de par de eventos foi executada usando o objeto de par de eventos de cliente/servidor específico do thread, mas nenhum objeto de par de eventos foi associado ao thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**erro \_ de \_ configuração do CTRL do domínio de \_ erros \_**
</dt> <dd> <dl> <dt>

581 (0x245)
</dt> <dt>



Um Windows Server tem uma configuração incorreta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**\_caractere inválido de erro \_**
</dt> <dd> <dl> <dt>

582 (0x246)
</dt> <dt>



Um caractere inválido foi encontrado. Para um conjunto de caracteres de vários bytes, isso inclui um byte de Lead sem um byte de trilha com sucesso. Para o conjunto de caracteres Unicode, isso inclui os caracteres 0xFFFF e 0xFFFE.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERRO de \_ caractere INdefinido \_**
</dt> <dd> <dl> <dt>

583 (0x247)
</dt> <dt>



O caractere Unicode não está definido no conjunto de caracteres Unicode instalado no sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERRO \_ de \_ volume de disquete**
</dt> <dd> <dl> <dt>

584 (0x248)
</dt> <dt>



O arquivo de paginação não pode ser criado em um disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERRO o \_ BIOS \_ falhou ao \_ \_ conectar a \_ interrupção**
</dt> <dd> <dl> <dt>

585 (0x249)
</dt> <dt>



O BIOS do sistema falhou ao conectar uma interrupção do sistema ao dispositivo ou ao barramento para o qual o dispositivo está conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERRO \_ no \_ controlador de backup**
</dt> <dd> <dl> <dt>

586 (0x24A)
</dt> <dt>



Esta operação só é permitida para o controlador de domínio primário do domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**limite de Mutant de erro \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

587 (0x24B)
</dt> <dt>



Foi feita uma tentativa de adquirir um Mutant de modo que sua contagem máxima teria sido excedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**Driver de erro \_ FS \_ \_ necessário**
</dt> <dd> <dl> <dt>

588 (0x24C)
</dt> <dt>



Um volume foi acessado para o qual um driver de sistema de arquivos é necessário e ainda não foi carregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERRO \_ não é possível \_ carregar o \_ arquivo do registro \_**
</dt> <dd> <dl> <dt>

589 (0x24D)
</dt> <dt>



{Falha no arquivo do registro} O registro não pode carregar o hive (arquivo):% HS ou seu log ou alternativo. Ele está corrompido, ausente ou não é gravável.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERRO \_ \_ ao anexar a depuração \_**
</dt> <dd> <dl> <dt>

590 (0x24E)
</dt> <dt>



{Falha inesperada em [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Ocorreu uma falha inesperada ao processar uma solicitação de API **DebugActiveProcess** . Você pode escolher OK para encerrar o processo ou cancelar para ignorar o erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**processo do sistema de erros \_ \_ \_ encerrado**
</dt> <dd> <dl> <dt>

591 (0x24F)
</dt> <dt>



{Erro fatal do sistema} O processo do sistema% HS foi finalizado inesperadamente com um status de 0x% 08x (0x% 08x 0x% 08x). O sistema foi desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**dados de erro \_ \_ não \_ aceitos**
</dt> <dd> <dl> <dt>

592 (0x250)
</dt> <dt>



{Dados não aceitos} O cliente TDI não pôde manipular os dados recebidos durante uma indicação.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**erro \_ de \_ erro de hardware do VDM \_**
</dt> <dd> <dl> <dt>

593 (0x251)
</dt> <dt>



NTVDM encontrou um erro de hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERRO \_ ao \_ cancelar o \_ tempo limite de driver**
</dt> <dd> <dl> <dt>

594 (0x252)
</dt> <dt>



{Cancelar tempo limite} O driver% hs não pôde concluir uma solicitação de e/s cancelada no tempo alocado.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**incompatibilidade de mensagem de resposta de erro \_ \_ \_**
</dt> <dd> <dl> <dt>

595 (0x253)
</dt> <dt>



{Incompatibilidade de mensagem de resposta} Foi feita uma tentativa de responder a uma mensagem de LPC, mas o thread especificado pela ID do cliente na mensagem não estava aguardando essa mensagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERRO \_ ao \_ perder \_ dados de WRITEBEHIND**
</dt> <dd> <dl> <dt>

596 (0x254)
</dt> <dt>



{Falha na gravação atrasada} O Windows não pôde salvar todos os dados do arquivo% hs. Os dados foram perdidos. Esse erro pode ser causado por uma falha de conexão de rede ou de hardware do seu computador. Tente salvar este arquivo em outro lugar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERRO \_ de \_ parâmetros do servidor cliente \_ \_ inválido**
</dt> <dd> <dl> <dt>

597 (0x255)
</dt> <dt>



Os parâmetros passados para o servidor na janela de memória compartilhada do cliente/servidor eram inválidos. Muitos dados podem ter sido colocados na janela de memória compartilhada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERRO \_ sem \_ \_ fluxo pequeno**
</dt> <dd> <dl> <dt>

598 (0x256)
</dt> <dt>



O fluxo não é um pequeno fluxo.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**\_leitura de \_ estouro de pilha de erros \_**
</dt> <dd> <dl> <dt>

599 (0x257)
</dt> <dt>



A solicitação deve ser manipulada pelo código de estouro de pilha.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERRO ao \_ Converter \_ em \_ grande**
</dt> <dd> <dl> <dt>

600 (0x258)
</dt> <dt>



Códigos de status internos do OFS indicando como uma operação de alocação é manipulada. Ele é repetido depois que o onode que o contém é movido ou o fluxo de extensão é convertido em um fluxo grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERRO \_ encontrado \_ fora \_ do \_ escopo**
</dt> <dd> <dl> <dt>

601 (0x259)
</dt> <dt>



A tentativa de localizar o objeto encontrou uma correspondência de objeto por ID no volume, mas está fora do escopo do identificador usado para a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERRO ao \_ alocar \_ Bucket**
</dt> <dd> <dl> <dt>

602 (0x25A)
</dt> <dt>



A matriz de buckets deve ser expandida. Repita a transação depois de fazer isso.


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**\_estouro de Marshall de erro \_**
</dt> <dd> <dl> <dt>

603 (0x25B)
</dt> <dt>



O buffer de Marshalling de usuário/kernel estourou.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERRO \_ de \_ variante inválida**
</dt> <dd> <dl> <dt>

604 (0x25C)
</dt> <dt>



A estrutura variante fornecida contém dados inválidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERRO \_ de \_ buffer de compactação insatisfatório \_**
</dt> <dd> <dl> <dt>

605 (0x25D)
</dt> <dt>



O buffer especificado contém dados mal formados.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**\_falha na auditoria de erro \_**
</dt> <dd> <dl> <dt>

606 (0x25E)
</dt> <dt>



{Falha na auditoria} Falha ao tentar gerar uma auditoria de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**resolução do timer de erro \_ \_ \_ não \_ definida**
</dt> <dd> <dl> <dt>

607 (0x25F)
</dt> <dt>



A resolução do temporizador não foi definida anteriormente pelo processo atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERRO \_ de \_ informações de logon insuficiente \_**
</dt> <dd> <dl> <dt>

608 (0x260)
</dt> <dt>



Não há informações de conta suficientes para fazer logon.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERRO \_ de \_ entrada de DLL inválido \_**
</dt> <dd> <dl> <dt>

609 (0x261)
</dt> <dt>



{Ponto de entrada DLL inválido} A biblioteca de vínculo dinâmico% hs não foi gravada corretamente. O ponteiro de pilha foi deixado em um estado inconsistente. O EntryPoint deve ser declarado como Winapi tenha ou STDCALL. Selecione Sim para falhar a carga da DLL. Selecione não para continuar a execução. Selecionar não pode fazer com que o aplicativo opere incorretamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERRO \_ de \_ ponto de entrada de serviço insatisfatório \_**
</dt> <dd> <dl> <dt>

610 (0x262)
</dt> <dt>



{Ponto de entrada de retorno de serviço inválido} O serviço% hs não foi gravado corretamente. O ponteiro de pilha foi deixado em um estado inconsistente. O ponto de entrada de retorno de chamada deve ser declarado como Winapi tenha ou STDCALL. A seleção de OK fará com que o serviço continue a operação. No entanto, o processo de serviço pode funcionar incorretamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERRO \_ de \_ endereço IP \_ CONFLICT1**
</dt> <dd> <dl> <dt>

611 (0x263)
</dt> <dt>



Há um conflito de endereço IP com outro sistema na rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERRO \_ de \_ endereço IP \_ CONFLICT2**
</dt> <dd> <dl> <dt>

612 (0x264)
</dt> <dt>



Há um conflito de endereço IP com outro sistema na rede.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_limite de \_ cota de registro de erro \_**
</dt> <dd> <dl> <dt>

613 (0x265)
</dt> <dt>



{Pouco espaço no registro} O sistema atingiu o tamanho máximo permitido para a parte do sistema do registro. As solicitações de armazenamento adicionais serão ignoradas.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERRO \_ nenhum \_ retorno de chamada \_ ativo**
</dt> <dd> <dl> <dt>

614 (0x266)
</dt> <dt>



Um serviço do sistema de retorno de chamada de retorno não pode ser executado quando nenhum retorno de chamada está ativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERRO \_ pwd \_ muito \_ curto**
</dt> <dd> <dl> <dt>

615 (0x267)
</dt> <dt>



A senha fornecida é muito curta para atender à política de sua conta de usuário. Escolha uma senha mais longa.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERRO \_ pwd \_ muito \_ recente**
</dt> <dd> <dl> <dt>

616 (0x268)
</dt> <dt>



A política da sua conta de usuário não permite que você altere as senhas com muita frequência. Isso é feito para impedir que os usuários mudem de volta para uma senha familiar, mas potencialmente descoberta. Se você sentir que sua senha foi comprometida, entre em contato com o administrador imediatamente para ter uma nova atribuída.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**conflito de histórico de erro \_ pwd \_ \_**
</dt> <dd> <dl> <dt>

617 (0x269)
</dt> <dt>



Você tentou alterar sua senha para uma que já usou no passado. A política da sua conta de usuário não permite isso. Selecione uma senha que você não usou anteriormente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERRO de \_ \_ compactação sem suporte**
</dt> <dd> <dl> <dt>

618 (0x26A)
</dt> <dt>



O formato de compactação especificado não tem suporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERRO \_ de \_ perfil HW inválido \_**
</dt> <dd> <dl> <dt>

619 (0x26B)
</dt> <dt>



A configuração do perfil de hardware especificado é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERRO \_ de \_ \_ caminho de dispositivo PLUGPLAY inválido \_**
</dt> <dd> <dl> <dt>

620 (0x26C)
</dt> <dt>



O caminho do dispositivo do registro de Plug and Play especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**\_lista de cotas de erro \_ \_ inconsistente**
</dt> <dd> <dl> <dt>

621 (0x26D)
</dt> <dt>



A lista de cotas especificada é internamente inconsistente com seu descritor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**\_expiração da avaliação de erro \_**
</dt> <dd> <dl> <dt>

622 (0x26E)
</dt> <dt>



{Notificação de avaliação do Windows} O período de avaliação desta instalação do Windows expirou. Este sistema será desligado em 1 hora. Para restaurar o acesso a esta instalação do Windows, atualize esta instalação usando uma distribuição licenciada deste produto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERRO \_ de \_ \_ realocação de dll ilegal**
</dt> <dd> <dl> <dt>

623 (0x26F)
</dt> <dt>



{Realocação de DLL do sistema ilegal} A DLL do sistema% HS foi realocada na memória. O aplicativo não será executado corretamente. A realocação ocorreu porque a DLL% HS ocupava um intervalo de endereços reservado para DLLs de sistema do Windows. O fornecedor que fornece a DLL deve ser contatado para uma nova DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERRO \_ dll \_ init \_ falha ao fazer \_ logoff**
</dt> <dd> <dl> <dt>

624 (0x270)
</dt> <dt>



{Falha na inicialização da DLL} Falha ao inicializar o aplicativo porque a estação de janela está sendo desligada.


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERRO ao \_ validar a \_ continuação**
</dt> <dd> <dl> <dt>

625 (0x271)
</dt> <dt>



O processo de validação precisa continuar na próxima etapa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERRO \_ sem \_ mais \_ correspondências**
</dt> <dd> <dl> <dt>

626 (0x272)
</dt> <dt>



Não há mais correspondências para a enumeração de índice atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_conflito de \_ lista de intervalo de erros \_**
</dt> <dd> <dl> <dt>

627 (0x273)
</dt> <dt>



Não foi possível adicionar o intervalo à lista de intervalos devido a um conflito.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**incompatibilidade de \_ SID do servidor de erro \_ \_**
</dt> <dd> <dl> <dt>

628 (0x274)
</dt> <dt>



O processo do servidor está sendo executado sob um SID diferente daquele exigido pelo cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERRO não é possível \_ \_ habilitar \_ \_ somente negar**
</dt> <dd> <dl> <dt>

629 (0x275)
</dt> <dt>



Um grupo marcado como uso somente para negar não pode ser habilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERRO ao \_ flutuar \_ várias \_ falhas**
</dt> <dd> <dl> <dt>

630 (0x276)
</dt> <dt>



Exception Várias falhas de ponto flutuante.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERRO ao \_ flutuar \_ várias \_ interceptações**
</dt> <dd> <dl> <dt>

631 (0x277)
</dt> <dt>



Exception Várias interceptações de ponto flutuante.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERRO \_ NOinterface**
</dt> <dd> <dl> <dt>

632 (0x278)
</dt> <dt>



Não há suporte para a interface solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**\_ \_ falha no suspensão do driver de erro \_**
</dt> <dd> <dl> <dt>

633 (0x279)
</dt> <dt>



{Falha no sistema em espera} O driver% hs não dá suporte ao modo de espera. A atualização deste driver pode permitir que o sistema vá para o modo de espera.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERRO \_ \_ arquivo de sistema corrompido \_**
</dt> <dd> <dl> <dt>

634 (0x27A)
</dt> <dt>



O arquivo de sistema %1 se tornou corrompido e foi substituído.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_mínimo de compromisso de erro \_**
</dt> <dd> <dl> <dt>

635 (0x27B)
</dt> <dt>



{Memória virtual mínima muito baixa} O sistema está com pouca memória virtual. O Windows está aumentando o tamanho do arquivo de paginação da memória virtual. Durante esse processo, as solicitações de memória para alguns aplicativos podem ser negadas. Para obter mais informações, consulte a ajuda.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERRO \_ de \_ enumeração de reinício de PNP \_**
</dt> <dd> <dl> <dt>

636 (0x27C)
</dt> <dt>



Um dispositivo foi removido; portanto, A enumeração deve ser reiniciada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERRO \_ de \_ \_ assinatura inadequada da imagem do sistema \_**
</dt> <dd> <dl> <dt>

637 (0x27D)
</dt> <dt>



{Erro fatal do sistema} A imagem do sistema% s não está assinada corretamente. O arquivo foi substituído pelo arquivo assinado. O sistema foi desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERRO \_ de \_ reinicialização de PNP \_ necessária**
</dt> <dd> <dl> <dt>

638 (0x27E)
</dt> <dt>



O dispositivo não será iniciado sem uma reinicialização.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERRO \_ de \_ energia insuficiente**
</dt> <dd> <dl> <dt>

639 (0x27F)
</dt> <dt>



Não há energia suficiente para concluir a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERRO \_ de \_ várias \_ violações de falha**
</dt> <dd> <dl> <dt>

640 (0x280)
</dt> <dt>



ERRO \_ de \_ várias \_ violações de falha


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERRO \_ de \_ desligamento do sistema**
</dt> <dd> <dl> <dt>

641 (0x281)
</dt> <dt>



O sistema está em processo de desligamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**porta de erro \_ \_ não \_ definida**
</dt> <dd> <dl> <dt>

642 (0x282)
</dt> <dt>



Foi feita uma tentativa de remover DebugPort de processos, mas uma porta ainda não estava associada ao processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERRO \_ \_ na verificação da versão DS \_ \_**
</dt> <dd> <dl> <dt>

643 (0x283)
</dt> <dt>



Esta versão do Windows não é compatível com a versão de comportamento da floresta de diretório, domínio ou controlador de domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**intervalo de erros \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

644 (0x284)
</dt> <dt>



O intervalo especificado não foi encontrado na lista de intervalos.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERRO \_ não é um \_ \_ Driver de modo seguro \_**
</dt> <dd> <dl> <dt>

646 (0x286)
</dt> <dt>



O driver não foi carregado porque o sistema está sendo inicializado no modo de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERRO \_ de \_ entrada de driver com falha \_**
</dt> <dd> <dl> <dt>

647 (0x287)
</dt> <dt>



O driver não foi carregado porque falhou em sua chamada de inicialização.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**\_erro de \_ enumeração de dispositivo de erro \_**
</dt> <dd> <dl> <dt>

648 (0x288)
</dt> <dt>



"% Hs" encontrou um erro ao aplicar energia ou ler a configuração do dispositivo. Isso pode ser causado por uma falha de seu hardware ou por uma conexão ruim.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ponto de montagem do erro \_ \_ \_ não \_ resolvido**
</dt> <dd> <dl> <dt>

649 (0x289)
</dt> <dt>



A operação de criação falhou porque o nome continha pelo menos um ponto de montagem que é resolvido para um volume ao qual o objeto de dispositivo especificado não está anexado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERRO \_ de \_ \_ parâmetro de objeto de dispositivo inválido \_**
</dt> <dd> <dl> <dt>

650 (0x28A)
</dt> <dt>



O parâmetro de objeto do dispositivo não é um objeto de dispositivo válido ou não está anexado ao volume especificado pelo nome do arquivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERRO de \_ MCA \_ ocorrido**
</dt> <dd> <dl> <dt>

651 (0x28B)
</dt> <dt>



Ocorreu um erro de verificação de máquina. Consulte o log de eventos do sistema para obter informações adicionais.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**\_erro de \_ banco de dados de driver de erro \_**
</dt> <dd> <dl> <dt>

652 (0x28C)
</dt> <dt>



Erro \[ %2 ao \] processar o banco de dados do driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**o hive do sistema de erro é \_ \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

653 (0x28D)
</dt> <dt>



O tamanho do hive do sistema excedeu seu limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**\_ \_ falha no \_ \_ descarregamento anterior do driver de erro**
</dt> <dd> <dl> <dt>

654 (0x28E)
</dt> <dt>



Não foi possível carregar o driver porque uma versão anterior do driver ainda está na memória.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERRO \_ VOLSNAP \_ preparar \_ hibernação**
</dt> <dd> <dl> <dt>

655 (0x28F)
</dt> <dt>



{Serviço de Cópias de Sombra de Volume} Aguarde enquanto o Serviço de Cópias de Sombra de Volume prepara o volume% hs para hibernação.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**\_falha de hibernação de erro \_**
</dt> <dd> <dl> <dt>

656 (0x290)
</dt> <dt>



O sistema falhou ao hibernar (o código de erro é% HS). A hibernação será desabilitada até que o sistema seja reiniciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERRO \_ pwd \_ muito \_ longo**
</dt> <dd> <dl> <dt>

657 (0x291)
</dt> <dt>



A senha fornecida é muito longa para atender à política de sua conta de usuário. Escolha uma senha mais curta.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_limitação do \_ sistema de arquivos de erro \_**
</dt> <dd> <dl> <dt>

665 (0x299)
</dt> <dt>



Não foi possível concluir a operação solicitada devido a uma limitação do sistema de arquivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**\_falha na asserção de erro \_**
</dt> <dd> <dl> <dt>

668 (0x29C)
</dt> <dt>



Ocorreu uma falha de asserção.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**erro de \_ ACPI \_ erro**
</dt> <dd> <dl> <dt>

669 (0x29D)
</dt> <dt>



Ocorreu um erro no subsistema ACPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERRO \_ de \_ asserção Wow**
</dt> <dd> <dl> <dt>

670 (0x29E)
</dt> <dt>



Erro de asserção WOW.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERRO \_ PNP de uma \_ \_ tabela MPS inadequada \_**
</dt> <dd> <dl> <dt>

671 (0x29F)
</dt> <dt>



Um dispositivo está ausente na tabela MPS do BIOS do sistema. Este dispositivo não será usado. Entre em contato com o fornecedor do sistema para obter a atualização do BIOS do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERRO \_ \_ na conversão de PNP \_**
</dt> <dd> <dl> <dt>

672 (0x2A0)
</dt> <dt>



Um tradutor não pôde converter os recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERRO \_ \_ na conversão de IRQ de PNP \_ \_**
</dt> <dd> <dl> <dt>

673 (0x2A1)
</dt> <dt>



Um tradutor de IRQ falhou ao converter recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERRO de \_ ID de PNP \_ inválido \_**
</dt> <dd> <dl> <dt>

674 (0x2A2)
</dt> <dt>



O driver %2 retornou uma ID inválida para um dispositivo filho (%3).


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERRO \_ do \_ depurador do sistema de ativação \_**
</dt> <dd> <dl> <dt>

675 (0x2A3)
</dt> <dt>



{Kernel Debugger ativado} o depurador do sistema foi ativado por uma interrupção.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_identificadores de erro \_ fechados**
</dt> <dd> <dl> <dt>

676 (0x2A4)
</dt> <dt>



{Identificadores fechados} Identificadores para objetos foram fechados automaticamente como resultado da operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**\_informações incorretas sobre o erro \_**
</dt> <dd> <dl> <dt>

677 (0x2A5)
</dt> <dt>



{Excesso de informações} A lista de controle de acesso (ACL) especificada continha mais informações do que o esperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**confirmação de RXACT de erro \_ \_ \_ necessária**
</dt> <dd> <dl> <dt>

678 (0x2A6)
</dt> <dt>



Esse status de nível de aviso indica que o estado da transação já existe para a subárvore do registro, mas que uma confirmação de transação foi anulada anteriormente. A confirmação não foi concluída, mas não foi revertida (portanto, ela ainda pode ser confirmada se desejado).


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_verificação de mídia de erro \_**
</dt> <dd> <dl> <dt>

679 (0x2A7)
</dt> <dt>



{Mídia alterada} A mídia pode ter sido alterada.


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**substituição de GUID de erro \_ \_ \_ feita**
</dt> <dd> <dl> <dt>

680 (0x2A8)
</dt> <dt>



{Substituição de GUID} Durante a tradução de um identificador global (GUID) para uma ID de segurança (SID) do Windows, nenhum prefixo GUID definido administrativamente foi encontrado. Um prefixo substituto foi usado, o que não comprometerá a segurança do sistema. No entanto, isso pode fornecer um acesso mais restritivo do que o pretendido.


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERRO \_ interrompido \_ em \_ SYMLINK**
</dt> <dd> <dl> <dt>

681 (0x2A9)
</dt> <dt>



A operação de criação parou depois de atingir um link simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERRO \_ LONGJUMP**
</dt> <dd> <dl> <dt>

682 (0x2AA)
</dt> <dt>



Um salto longo foi executado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERRO \_ PLUGPLAY \_ consulta \_ vetada**
</dt> <dd> <dl> <dt>

683 (0x2AB)
</dt> <dt>



A operação de consulta de Plug and Play não foi bem-sucedida.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**reliberação de erro de \_ \_ desconsolidação**
</dt> <dd> <dl> <dt>

684 (0x2AC)
</dt> <dt>



Uma consolidação de quadros foi executada.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_hive do registro de erro \_ \_ recuperado**
</dt> <dd> <dl> <dt>

685 (0x2AD)
</dt> <dt>



{O hive do registro foi recuperado} Hive do registro (arquivo):% HS foi corrompido e foi recuperado. Alguns dados podem ter sido perdidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**DLL de erro \_ \_ pode \_ ser \_ inseguro**
</dt> <dd> <dl> <dt>

686 (0x2AE)
</dt> <dt>



O aplicativo está tentando executar o código executável do módulo% hs. Isso pode ser inseguro. Uma alternativa,% HS, está disponível. O aplicativo deve usar o módulo seguro% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**DLL de erro \_ \_ pode \_ ser \_ incompatível**
</dt> <dd> <dl> <dt>

687 (0x2AF)
</dt> <dt>



O aplicativo está carregando o código executável do módulo% hs. Isso é seguro, mas pode ser incompatível com as versões anteriores do sistema operacional. Uma alternativa,% HS, está disponível. O aplicativo deve usar o módulo seguro% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERRO \_ de \_ exceção DBG \_ não \_ tratada**
</dt> <dd> <dl> <dt>

688 (0x2B0)
</dt> <dt>



O depurador não resolveu a exceção.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERRO \_ DBG \_ responder \_ mais tarde**
</dt> <dd> <dl> <dt>

689 (0x2B1)
</dt> <dt>



O depurador será respondido mais tarde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERRO \_ DBG \_ não é possível \_ \_ fornecer \_ identificador**
</dt> <dd> <dl> <dt>

690 (0x2B2)
</dt> <dt>



O depurador não pode fornecer identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERRO \_ de \_ término do \_ thread DBG**
</dt> <dd> <dl> <dt>

691 (0x2B3)
</dt> <dt>



Thread encerrado pelo depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERRO \_ de \_ finalizar processo de DBG \_**
</dt> <dd> <dl> <dt>

692 (0x2B4)
</dt> <dt>



Processo finalizado pelo depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERRO \_ de \_ controle DBG \_ C**
</dt> <dd> <dl> <dt>

693 (0x2B5)
</dt> <dt>



O depurador obteve o controle C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERRO \_ DBG \_ com exceção \_ C**
</dt> <dd> <dl> <dt>

694 (0x2B6)
</dt> <dt>



O depurador imprimiu a exceção no controle C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERRO \_ DBG \_ RIPEXCEPTION**
</dt> <dd> <dl> <dt>

695 (0x2B7)
</dt> <dt>



O depurador recebeu uma exceção RIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERRO \_ de \_ quebra de controle DBG \_**
</dt> <dd> <dl> <dt>

696 (0x2B8)
</dt> <dt>



O depurador recebeu uma quebra de controle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERRO \_ de \_ exceção de comando DBG \_**
</dt> <dd> <dl> <dt>

697 (0x2B9)
</dt> <dt>



Exceção de comunicação de comando do depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**o \_ nome do objeto de erro \_ \_ existe**
</dt> <dd> <dl> <dt>

698 (0x2BA)
</dt> <dt>



{Objeto existe} Foi feita uma tentativa de criar um objeto e o nome do objeto já existia.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**o \_ thread de erro \_ foi \_ suspenso**
</dt> <dd> <dl> <dt>

699 (0x2BB)
</dt> <dt>



{Thread suspenso} Uma terminação de thread ocorreu enquanto o thread estava suspenso. O thread foi retomado e o encerramento foi continuado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_imagem \_ de erro não \_ na \_ base**
</dt> <dd> <dl> <dt>

700 (0x2BC)
</dt> <dt>



{Imagem realocada} Não foi possível mapear um arquivo de imagem no endereço especificado no arquivo de imagem. As correções locais devem ser executadas nesta imagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERRO \_ RXACT \_ estado \_ criado**
</dt> <dd> <dl> <dt>

701 (0x2BD)
</dt> <dt>



Esse status de nível informativo indica que um estado de transação de subárvore do registro especificado ainda não existia e teve que ser criado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notificação de segmento de erro \_**
</dt> <dd> <dl> <dt>

702 (0x2BE)
</dt> <dt>



{Carga do segmento} Uma máquina virtual de DOS (VDM) está carregando, descarregando ou movendo uma imagem de segmento de programa do MS-DOS ou Win16. Uma exceção é gerada para que um depurador possa carregar, descarregar ou rastrear símbolos e pontos de interrupção nesses segmentos de 16 bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERRO \_ de \_ diretório atual insatisfatório \_**
</dt> <dd> <dl> <dt>

703 (0x2BF)
</dt> <dt>



{Diretório atual inválido} O processo não pode mudar para o diretório atual de inicialização% hs. Selecione OK para definir o diretório atual como% HS ou selecione Cancelar para sair.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERRO \_ ft \_ Read \_ Recovery \_ do \_ backup**
</dt> <dd> <dl> <dt>

704 (0x2C0)
</dt> <dt>



{Leitura redundante} Para atender a uma solicitação de leitura, o sistema de arquivos tolerante a falhas do NT leu com êxito os dados solicitados de uma cópia redundante. Isso foi feito porque o sistema de arquivos encontrou uma falha em um membro do volume tolerante a falhas, mas não pôde reatribuir a área com falha do dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERRO \_ ft \_ de \_ recuperação de gravação**
</dt> <dd> <dl> <dt>

705 (0x2C1)
</dt> <dt>



{Gravação redundante} Para atender a uma solicitação de gravação, o sistema de arquivos tolerante a falhas do NT escreveu com êxito uma cópia redundante das informações. Isso foi feito porque o sistema de arquivos encontrou uma falha em um membro do volume tolerante a falhas, mas não pôde reatribuir a área com falha do dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**tipo de máquina de imagem de erro \_ \_ \_ \_ incompatível**
</dt> <dd> <dl> <dt>

706 (0x2C2)
</dt> <dt>



{Tipo de computador não compatível} O arquivo de imagem% HS é válido, mas é para um tipo de computador diferente do computador atual. Selecione OK para continuar ou cancelar para falhar a carga da DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERRO ao \_ receber \_ parcial**
</dt> <dd> <dl> <dt>

707 (0x2C3)
</dt> <dt>



{Dados parciais recebidos} O transporte de rede retornou dados parciais para seu cliente. Os dados restantes serão enviados mais tarde.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERRO ao \_ receber \_ acelerado**
</dt> <dd> <dl> <dt>

708 (0x2C4)
</dt> <dt>



{Dados emitidos recebidos} O transporte de rede retornou dados para seu cliente que foi marcado como emitido pelo sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERRO \_ ao \_ receber \_ acelerado parcial**
</dt> <dd> <dl> <dt>

709 (0x2C5)
</dt> <dt>



{Dados parciais expedidos recebidos} O transporte de rede retornou dados parciais para seu cliente e esses dados foram marcados como emitidos pelo sistema remoto. Os dados restantes serão enviados mais tarde.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**evento de erro \_ \_ concluído**
</dt> <dd> <dl> <dt>

710 (0x2C6)
</dt> <dt>



{Evento TDI concluído} A indicação de TDI foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**evento de erro \_ \_ pendente**
</dt> <dd> <dl> <dt>

711 (0x2C7)
</dt> <dt>



{Evento TDI pendente} A indicação de TDI entrou no estado pendente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERRO ao \_ verificar o \_ sistema de arquivos \_**
</dt> <dd> <dl> <dt>

712 (0x2C8)
</dt> <dt>



Verificando o sistema de arquivos em% wZ.


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERRO \_ fatal do \_ aplicativo de \_ saída**
</dt> <dd> <dl> <dt>

713 (0x2C9)
</dt> <dt>



{Saída fatal do aplicativo}% hs.


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**identificador de erro \_ predefinido \_**
</dt> <dd> <dl> <dt>

714 (0x2CA)
</dt> <dt>



A chave do Registro especificada é referenciada por um identificador predefinido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERRO \_ \_ desbloqueado**
</dt> <dd> <dl> <dt>

715 (0x2CB)
</dt> <dt>



{Página desbloqueada} A proteção de página de uma página bloqueada foi alterada para ' sem acesso ' e a página foi desbloqueada da memória e do processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notificação do serviço de erro \_**
</dt> <dd> <dl> <dt>

716 (0x2CC)
</dt> <dt>



% HS


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERRO \_ \_ bloqueado**
</dt> <dd> <dl> <dt>

717 (0x2CD)
</dt> <dt>



{Página bloqueada} Uma das páginas a serem bloqueadas já estava bloqueada.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_erro de \_ hardware do log de erros \_**
</dt> <dd> <dl> <dt>

718 (0x2CE)
</dt> <dt>



Pop-up de aplicativo: %1: %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERRO \_ já \_ Win32**
</dt> <dd> <dl> <dt>

719 (0x2CF)
</dt> <dt>



ERRO \_ já \_ Win32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**tipo de máquina de imagem de erro de não \_ \_ \_ \_ correspondência \_ exe**
</dt> <dd> <dl> <dt>

720 (0x2D0)
</dt> <dt>



{Tipo de computador não compatível} O arquivo de imagem% HS é válido, mas é para um tipo de computador diferente do computador atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERRO \_ sem \_ rendimento \_ realizado**
</dt> <dd> <dl> <dt>

721 (0x2D1)
</dt> <dt>



Uma execução de yield foi executada e nenhum thread estava disponível para execução.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**retomada do timer de erro \_ \_ \_ ignorada**
</dt> <dd> <dl> <dt>

722 (0x2D2)
</dt> <dt>



O sinalizador retomável para uma API de timer foi ignorado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERRO de \_ arbitragem \_ sem tratamento**
</dt> <dd> <dl> <dt>

723 (0x2D3)
</dt> <dt>



O arbitrador tem deferida a arbitragem desses recursos para seu pai.


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERRO \_ CardBus \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

724 (0x2D4)
</dt> <dt>



O dispositivo CardBus inserido não pode ser iniciado devido a um erro de configuração em "% hs".


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERRO \_ MP \_ \_ incompatível do processador**
</dt> <dd> <dl> <dt>

725 (0x2D5)
</dt> <dt>



As CPUs nesse sistema multiprocessador não são do mesmo nível de revisão. Para usar todos os processadores, o sistema operacional se restringe aos recursos do processador menos capaz no sistema. Se ocorrerem problemas com este sistema, entre em contato com o fabricante da CPU para ver se há suporte para essa combinação de processadores.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERRO \_ hibernado**
</dt> <dd> <dl> <dt>

726 (0x2D6)
</dt> <dt>



O sistema foi colocado em hibernação.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERRO \_ retomar \_ hibernação**
</dt> <dd> <dl> <dt>

727 (0x2D7)
</dt> <dt>



O sistema foi retomado da hibernação.


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**FIRMWARE de erro \_ \_ atualizado**
</dt> <dd> <dl> <dt>

728 (0x2D8)
</dt> <dt>



O Windows detectou que o firmware do sistema (BIOS) foi atualizado na \[ data do firmware anterior = %2, data atual do firmware %3 \] .


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**DRIVERS de erro \_ \_ vazando \_ páginas bloqueadas \_**
</dt> <dd> <dl> <dt>

729 (0x2D9)
</dt> <dt>



Um driver de dispositivo está vazando páginas de e/s bloqueadas causando degradação do sistema. O sistema habilitou automaticamente o código de rastreamento para tentar detectar o culpado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERRO \_ ao \_ sistema de ativação**
</dt> <dd> <dl> <dt>

730 (0x2DA)
</dt> <dt>



O sistema tem acordado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERRO de \_ espera \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2DB)
</dt> <dt>



ERRO de \_ espera \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERRO de \_ espera \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2DC)
</dt> <dt>



ERRO de \_ espera \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERRO de \_ espera \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2DD)
</dt> <dt>



ERRO de \_ espera \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERRO ao \_ aguardar \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2DE)
</dt> <dt>



ERRO ao \_ aguardar \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERRO \_ abandonado- \_ aguardando \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2DF)
</dt> <dt>



ERRO \_ abandonado- \_ aguardando \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**Erro \_ abandonado ao \_ aguardar \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2E0)
</dt> <dt>



Erro \_ abandonado ao \_ aguardar \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERRO \_ de \_ APC do usuário**
</dt> <dd> <dl> <dt>

737 (0x2E1)
</dt> <dt>



ERRO \_ de \_ APC do usuário


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERRO do \_ kernel \_ APC**
</dt> <dd> <dl> <dt>

738 (0x2E2)
</dt> <dt>



ERRO do \_ kernel \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERRO \_ alertado**
</dt> <dd> <dl> <dt>

739 (0x2E3)
</dt> <dt>



ERRO \_ alertado


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**elevação de erro \_ \_ necessária**
</dt> <dd> <dl> <dt>

740 (0x2E4)
</dt> <dt>



A operação solicitada requer elevação.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERRO de \_ nova análise**
</dt> <dd> <dl> <dt>

741 (0x2E5)
</dt> <dt>



Uma nova análise deve ser executada pelo Gerenciador de objetos, pois o nome do arquivo resultou em um link simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERRO \_ \_ de bloqueio \_ de oplock em \_ andamento**
</dt> <dd> <dl> <dt>

742 (0x2E6)
</dt> <dt>



Uma operação abrir/criar foi concluída enquanto uma interrupção de oplock está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**VOLUME de erro \_ \_ montado**
</dt> <dd> <dl> <dt>

743 (0x2E7)
</dt> <dt>



Um novo volume foi montado por um sistema de arquivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERRO \_ RXACT \_ confirmado**
</dt> <dd> <dl> <dt>

744 (0x2E8)
</dt> <dt>



Esse status de nível de êxito indica que o estado da transação já existe para a subárvore do registro, mas que uma confirmação de transação foi anulada anteriormente. A confirmação já foi concluída.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**\_aviso de notificação de erro \_**
</dt> <dd> <dl> <dt>

745 (0x2E9)
</dt> <dt>



Isso indica que uma solicitação notificar alteração foi concluída devido ao fechamento do identificador que fez a solicitação notificar alteração.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERRO \_ ao \_ conectar o transporte primário \_ \_ falhou**
</dt> <dd> <dl> <dt>

746 (0x2EA)
</dt> <dt>



{Falha no Connect no transporte primário} Foi feita uma tentativa de conexão com o servidor remoto% hs no transporte primário, mas a conexão falhou. O computador foi capaz de se conectar em um transporte secundário.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transição de \_ falha de página de erro \_**
</dt> <dd> <dl> <dt>

747 (0x2EB)
</dt> <dt>



A falha de página era uma falha de transição.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERRO \_ de \_ solicitação de falha de página \_ \_ zero**
</dt> <dd> <dl> <dt>

748 (0x2EC)
</dt> <dt>



A falha de página era uma falha de demanda zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**\_ \_ falha \_ na cópia da página de erro \_ na \_ gravação**
</dt> <dd> <dl> <dt>

749 (0x2ED)
</dt> <dt>



A falha de página era uma falha de demanda zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**\_página de \_ proteção de falha da página de \_ erro \_**
</dt> <dd> <dl> <dt>

750 (0x2EE)
</dt> <dt>



A falha de página era uma falha de demanda zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_arquivo de \_ \_ paginação de falha de página de erro \_**
</dt> <dd> <dl> <dt>

751 (0x2EF)
</dt> <dt>



A falha de página foi satisfeita pela leitura de um dispositivo de armazenamento secundário.


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**página de cache de erro \_ \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

752 (0x2F0)
</dt> <dt>



A página armazenada em cache foi bloqueada durante a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**\_despejo de falha de erro \_**
</dt> <dd> <dl> <dt>

753 (0x2F1)
</dt> <dt>



O despejo de memória existe no arquivo de paginação.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**BUFFER de erros \_ \_ todos os \_ zeros**
</dt> <dd> <dl> <dt>

754 (0x2F2)
</dt> <dt>



O buffer especificado contém todos os zeros.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERRO ao \_ reanalisar \_ objeto**
</dt> <dd> <dl> <dt>

755 (0x2F3)
</dt> <dt>



Uma nova análise deve ser executada pelo Gerenciador de objetos, pois o nome do arquivo resultou em um link simbólico.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**requisitos de recursos de erro \_ \_ \_ alterados**
</dt> <dd> <dl> <dt>

756 (0x2F4)
</dt> <dt>



O dispositivo teve êxito em uma parada de consulta e seus requisitos de recursos foram alterados.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERRO de \_ conversão \_ concluída**
</dt> <dd> <dl> <dt>

757 (0x2F5)
</dt> <dt>



O tradutor converteu esses recursos no espaço global e nenhuma tradução adicional deve ser executada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERRO \_ nada \_ para \_ terminar**
</dt> <dd> <dl> <dt>

758 (0x2F6)
</dt> <dt>



Um processo que está sendo encerrado não tem threads para encerrar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**o \_ processo \_ de erro não está \_ no \_ trabalho**
</dt> <dd> <dl> <dt>

759 (0x2F7)
</dt> <dt>



O processo especificado não faz parte de um trabalho.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_processo \_ de erro no \_ trabalho**
</dt> <dd> <dl> <dt>

760 (0x2F8)
</dt> <dt>



O processo especificado faz parte de um trabalho.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERRO \_ de \_ hibernação de VOLSNAP \_ pronto**
</dt> <dd> <dl> <dt>

761 (0x2F9)
</dt> <dt>



{Serviço de Cópias de Sombra de Volume} O sistema agora está pronto para hibernação.


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERRO \_ FSFILTER \_ op \_ concluído \_ com êxito**
</dt> <dd> <dl> <dt>

762 (0x2FA)
</dt> <dt>



Um sistema de arquivos ou driver de filtro do sistema de arquivos concluiu com êxito uma operação FsFilter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**vetor de interrupção de erro \_ \_ \_ já \_ conectado**
</dt> <dd> <dl> <dt>

763 (0x2FB)
</dt> <dt>



O vetor de interrupção especificado já estava conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**interrupção de erro \_ \_ ainda \_ conectada**
</dt> <dd> <dl> <dt>

764 (0x2FC)
</dt> <dt>



O vetor de interrupção especificado ainda está conectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERRO ao \_ aguardar \_ \_ oplock**
</dt> <dd> <dl> <dt>

765 (0x2FD)
</dt> <dt>



Uma operação está bloqueada aguardando um oplock.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERRO \_ de \_ tratamento da exceção DBG \_**
</dt> <dd> <dl> <dt>

766 (0x2FE)
</dt> <dt>



Exceção manipulada pelo depurador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERRO \_ DBG \_ continuar**
</dt> <dd> <dl> <dt>

767 (0x2FF)
</dt> <dt>



O depurador continuou.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERRO \_ na \_ pilha pop de retorno de chamada \_**
</dt> <dd> <dl> <dt>

768 (0x300)
</dt> <dt>



Ocorreu uma exceção em um retorno de chamada de modo de usuário e o quadro de retorno de chamada do kernel deve ser removido.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**\_compactação de erro \_ desabilitada**
</dt> <dd> <dl> <dt>

769 (0x301)
</dt> <dt>



A compactação está desabilitada para este volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERRO \_ CANTFETCHBACKWARDS**
</dt> <dd> <dl> <dt>

770 (0x302)
</dt> <dt>



O provedor de dados não pode buscar versões anteriores por meio de um conjunto de resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERRO \_ CANTSCROLLBACKWARDS**
</dt> <dd> <dl> <dt>

771 (0x303)
</dt> <dt>



O provedor de dados não pode rolar para trás por meio de um conjunto de resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERRO \_ ROWSNOTRELEASED**
</dt> <dd> <dl> <dt>

772 (0x304)
</dt> <dt>



O provedor de dados requer que os dados previamente buscados sejam liberados antes de solicitar mais dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERRO \_ de \_ sinalizadores de assessor inválidos \_**
</dt> <dd> <dl> <dt>

773 (0x305)
</dt> <dt>



O provedor de dados não pôde interpretar os sinalizadores definidos para uma associação de coluna em um acessador.


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**erros de erro \_ \_ encontrados**
</dt> <dd> <dl> <dt>

774 (0x306)
</dt> <dt>



Um ou mais erros ocorreram durante o processamento da solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERRO \_ não \_ compatível**
</dt> <dd> <dl> <dt>

775 (0x307)
</dt> <dt>



A implementação não é capaz de executar a solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_solicitação \_ de erro fora \_ de \_ sequência**
</dt> <dd> <dl> <dt>

776 (0x308)
</dt> <dt>



O cliente de um componente solicitou uma operação que não é válida, dado o estado da instância do componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**\_erro de \_ análise da versão do erro \_**
</dt> <dd> <dl> <dt>

777 (0x309)
</dt> <dt>



Não foi possível analisar um número de versão.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERRO \_ BADSTARTPOSITION**
</dt> <dd> <dl> <dt>

778 (0x30A)
</dt> <dt>



A posição inicial do iterador é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_hardware de memória de erro \_**
</dt> <dd> <dl> <dt>

779 (0x30B)
</dt> <dt>



O hardware relatou um erro de memória não corrigível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**reparo do disco de erro \_ \_ \_ desabilitado**
</dt> <dd> <dl> <dt>

780 (0x30C)
</dt> <dt>



A operação tentada exigiu auto-recuperação para ser habilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERRO \_ \_ de recurso insuficiente \_ para o \_ \_ tamanho de seção compartilhada especificado \_ \_**
</dt> <dd> <dl> <dt>

781 (0x30D)
</dt> <dt>



O heap de área de trabalho encontrou um erro ao alocar memória de sessão. Há mais informações no log de eventos do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERRO \_ de \_ transição do PowerState do sistema \_**
</dt> <dd> <dl> <dt>

782 (0x30E)
</dt> <dt>



O estado de energia do sistema está em transição de %2 para %3.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERRO \_ de \_ \_ transição complexa do PowerState do sistema \_**
</dt> <dd> <dl> <dt>

783 (0x30F)
</dt> <dt>



O estado de energia do sistema está em transição de %2 para %3, mas pode inserir %4.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERRO \_ de \_ exceção de MCA**
</dt> <dd> <dl> <dt>

784 (0x310)
</dt> <dt>



Um thread está sendo expedido com exceção de MCA devido ao MCA.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERRO \_ \_ de auditoria \_ de acesso por \_ política**
</dt> <dd> <dl> <dt>

785 (0x311)
</dt> <dt>



O acesso a %1 é monitorado pela regra de política %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERRO \_ \_ de acesso desabilitado \_ não é uma \_ \_ interface do usuário mais segura \_ por \_ política**
</dt> <dd> <dl> <dt>

786 (0x312)
</dt> <dt>



O acesso a %1 foi restringido pelo administrador pela regra de política %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERRO \_ abandonar \_ HIBERFILE**
</dt> <dd> <dl> <dt>

787 (0x313)
</dt> <dt>



Um arquivo de hibernação válido foi invalidado e deve ser abandonado.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERRO \_ perdido \_ a \_ rede de dados WRITEBEHIND \_ \_ desconectada**
</dt> <dd> <dl> <dt>

788 (0x314)
</dt> <dt>



{Falha na gravação atrasada} O Windows não pôde salvar todos os dados para o arquivo% HS; os dados foram perdidos. Esse erro pode ser causado por problemas de conectividade de rede. Tente salvar este arquivo em outro lugar.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERRO \_ perdido \_ \_ \_ \_ erro do servidor de rede de dados WRITEBEHIND \_**
</dt> <dd> <dl> <dt>

789 (0x315)
</dt> <dt>



{Falha na gravação atrasada} O Windows não pôde salvar todos os dados para o arquivo% HS; os dados foram perdidos. Esse erro foi retornado pelo servidor no qual o arquivo existe. Tente salvar este arquivo em outro lugar.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERRO \_ perdido \_ WRITEBEHIND \_ de \_ disco local de dados \_ \_**
</dt> <dd> <dl> <dt>

790 (0x316)
</dt> <dt>



{Falha na gravação atrasada} O Windows não pôde salvar todos os dados para o arquivo% HS; os dados foram perdidos. Esse erro pode ser causado se o dispositivo tiver sido removido ou se a mídia estiver protegida contra gravação.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERRO \_ de \_ tabela MCFG inadequada \_**
</dt> <dd> <dl> <dt>

791 (0x317)
</dt> <dt>



Os recursos necessários para este dispositivo estão em conflito com a tabela MCFG.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERRO \_ de \_ reparo de disco \_ Redirecionado**
</dt> <dd> <dl> <dt>

792 (0x318)
</dt> <dt>



Não foi possível executar o reparo de volume enquanto ele estiver online. Agende para colocar o volume offline para que ele possa ser reparado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERRO \_ de \_ reparo de disco \_ malsucedido**
</dt> <dd> <dl> <dt>

793 (0x319)
</dt> <dt>



O reparo do volume não foi bem-sucedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERRO \_ de \_ log CORROMPIdo \_ cheio**
</dt> <dd> <dl> <dt>

794 (0x31A)
</dt> <dt>



Um dos logs de corrupção de volume está cheio. Outras corrupções que podem ser detectadas não serão registradas em log.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERRO \_ de \_ log corrompido \_ corrompido**
</dt> <dd> <dl> <dt>

795 (0x31B)
</dt> <dt>



Um dos logs de corrupção de volume está internamente corrompido e precisa ser recriado. O volume pode conter corrupções não detectadas e deve ser verificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERRO \_ de \_ log corrompido \_ indisponível**
</dt> <dd> <dl> <dt>

796 (0x31C)
</dt> <dt>



Um dos logs de corrupção de volume está indisponível para ser operado no.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERRO \_ log corrompido \_ \_ excluído \_ cheio**
</dt> <dd> <dl> <dt>

797 (0x31D)
</dt> <dt>



Um dos logs de corrupção de volume foi excluído enquanto ainda tem registros de corrupção neles. O volume contém danos detectados e deve ser verificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERRO \_ log corrompido \_ \_ limpo**
</dt> <dd> <dl> <dt>

798 (0x31E)
</dt> <dt>



Um dos logs de corrupção de volume foi limpo pelo Chkdsk e não contém mais danos reais.


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERRO \_ de \_ nome órfã \_ esgotado**
</dt> <dd> <dl> <dt>

799 (0x31F)
</dt> <dt>



Existem arquivos órfãos no volume, mas não foi possível recuperá-los porque não foi possível criar mais nomes novos no diretório de recuperação. Os arquivos devem ser movidos do diretório de recuperação.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERRO \_ oplock \_ alternado \_ para o \_ novo \_ identificador**
</dt> <dd> <dl> <dt>

800 (0x320)
</dt> <dt>



O oplock que estava associado a esse identificador agora está associado a um identificador diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERRO \_ não é possível \_ conceder o \_ \_ oplock solicitado**
</dt> <dd> <dl> <dt>

801 (0x321)
</dt> <dt>



Não é possível conceder um oplock do nível solicitado. Um oplock de um nível inferior pode estar disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERRO \_ não é possível \_ interromper o \_ oplock**
</dt> <dd> <dl> <dt>

802 (0x322)
</dt> <dt>



A operação não foi concluída com êxito porque isso causaria a interrupção de um oplock. O chamador solicitou que oplocks existentes não sejam quebrados.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**identificador de oplock de erro \_ \_ \_ fechado**
</dt> <dd> <dl> <dt>

803 (0x323)
</dt> <dt>



O identificador ao qual este oplock estava associado foi fechado. O oplock agora está danificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERRO \_ sem \_ condição de Ace \_**
</dt> <dd> <dl> <dt>

804 (0x324)
</dt> <dt>



A entrada de controle de acesso (ACE) especificada não contém uma condição.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERRO \_ de \_ condição Ace inválida \_**
</dt> <dd> <dl> <dt>

805 (0x325)
</dt> <dt>



A entrada de controle de acesso (ACE) especificada contém uma condição inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**identificador de arquivo de erro \_ \_ \_ revogado**
</dt> <dd> <dl> <dt>

806 (0x326)
</dt> <dt>



O acesso ao identificador de arquivo especificado foi revogado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_imagem \_ de erro em uma \_ \_ base diferente**
</dt> <dd> <dl> <dt>

807 (0x327)
</dt> <dt>



Um arquivo de imagem foi mapeado em um endereço diferente daquele especificado no arquivo de imagem, mas as correções ainda serão executadas automaticamente na imagem.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERRO \_ de \_ acesso de ea \_ negado**
</dt> <dd> <dl> <dt>

994 (0x3E2)
</dt> <dt>



O acesso ao atributo estendido foi negado.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**operação de erro \_ \_ anulada**
</dt> <dd> <dl> <dt>

995 (0x3E3)
</dt> <dt>



A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**\_e/s de erro \_ incompleta**
</dt> <dd> <dl> <dt>

996 (0x3E4)
</dt> <dt>



O evento de e/s sobreposto não está em um estado sinalizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**\_e/s de erro \_ pendente**
</dt> <dd> <dl> <dt>

997 (0x3E5)
</dt> <dt>



A operação de e/s sobreposta está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERRO \_ NOaccess**
</dt> <dd> <dl> <dt>

998 (0x3E6)
</dt> <dt>



Acesso inválido ao local da memória.


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERRO \_ SWAPERROR**
</dt> <dd> <dl> <dt>

999 (0x3E7)
</dt> <dt>



Erro ao executar operação de inpágina.


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

 

 
