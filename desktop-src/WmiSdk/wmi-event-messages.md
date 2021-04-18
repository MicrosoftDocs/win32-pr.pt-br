---
description: A lista a seguir lista os eventos com suporte nos logs WMI no Windows Vista e sistemas operacionais posteriores.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Mensagens de evento WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780680"
---
# <a name="wmi-event-messages"></a>Mensagens de evento WMI

A lista a seguir lista os eventos com suporte nos logs WMI no Windows Vista e sistemas operacionais posteriores.

> [!Note]  
> A documentação a seguir foi projetada para desenvolvedores e administradores de ti. Se você estiver tentando resolver uma mensagem de erro WMI em seu sistema doméstico, consulte o site [suporte da Microsoft](https://support.microsoft.com/) .

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_repositório WBEM \_ MC \_ inconsistente**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



O serviço de Instrumentação de Gerenciamento do Windows detectou uma inconsistência com o repositório WMI no diretório *% windir% \\ System32 \\ WBEM \\ Repository* e não pôde recuperá-lo. O repositório WMI será excluído agora, um novo repositório será criado com base no mecanismo de recuperação automática.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_carga do \_ \_ provedor do subsistema \_ LOCALSYSTEM do \_ provedor WBEM MC \_**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Um provedor, %1, foi registrado no namespace Instrumentação de Gerenciamento do Windows %2 para usar a conta LocalSystem. Essa conta é privilegiada e o provedor pode causar uma violação de segurança se não representar corretamente as solicitações do usuário.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM \_ MC \_ MOF \_ não \_ carregado \_ na \_ recuperação**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Erro %1 encontrado ao tentar carregar o MOF %2 durante a recuperação. Arquivo MOF marcado com AutoRecuperação.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**o WBEM \_ MC \_ não pode \_ ativar o \_ filtro**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



Não foi possível reativar o filtro de eventos com a consulta "%2" no namespace "%1" devido ao erro %3. Os eventos não podem ser entregues por meio desse filtro até que o problema seja corrigido.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_consulta do \_ \_ provedor de eventos inválido WBEM MC \_ \_**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



O provedor de eventos %1 tentou registrar uma consulta sintaticamente inválida "%2". A consulta será ignorada. A consulta pode ser corrigida examinando o repositório WMI com o CIM Studio e atualizando as assinaturas permanentes para o provedor e a consulta listados. Se a assinatura permanente for criada com o arquivo MOF que vem com um produto instalado, o fornecedor do aplicativo deverá ser contatado para corrigir o registro com falha.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ consulta intrínseca do provedor de eventos inválido \_ \_ WBEM MC**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



O provedor de eventos %1 tentou registrar uma consulta de evento intrínseca "%2" no namespace %3 para o qual o conjunto de classes de objeto de destino não pôde ser determinado. A consulta será ignorada.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_consulta do provedor de eventos WBEM MC \_ \_ \_ \_ muito \_ ampla**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



O provedor de eventos %1 tentou registrar a consulta "%2" no namespace %3, o que é muito amplo. Os provedores de eventos não podem fornecer eventos que são fornecidos pelo sistema. A consulta será ignorada. Contate o fornecedor do aplicativo.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_consulta do provedor de eventos WBEM MC \_ \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



O provedor de eventos %1 tentou registrar a consulta "%2" cuja classe de destino "%3" no namespace %4 não existe. A consulta será ignorada.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_consulta do provedor de eventos WBEM MC \_ \_ \_ \_ não \_ evento**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



O provedor de eventos %1 tentou registrar a consulta &quot; %2 &quot; cuja classe de destino &quot; %3 &quot; não é uma classe de evento. A consulta será ignorada. Contate o fornecedor do aplicativo.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**falha de núcleo do WBEM \_ MC \_ WBEM \_ \_**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



Falha ao inicializar o núcleo do WMI ou o subsistema do provedor ou o subsistema de eventos com o número de erro %1. Isso pode ser devido a uma versão mal instalada do WMI, falha na atualização do repositório WMI, espaço em disco insuficiente ou memória insuficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_ \_ \_ falha na conexão do WBEM MC ADAP \_**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Falha do ADAP Instrumentação de Gerenciamento do Windows ao se conectar ao namespace %1 com o seguinte erro %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**falha do WBEM \_ MC \_ ADAP \_ \_ PUTCLASS \_**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Instrumentação de Gerenciamento do Windows ADAP não pôde salvar o objeto %1 no namespace %2 devido ao seguinte erro %3.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ incapaz \_ de \_ Adicionar \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Instrumentação de Gerenciamento do Windows ADAP não pôde criar a \_ classe base de desempenho Win32 em %1: resultado = %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ incapaz \_ de \_ Adicionar \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Instrumentação de Gerenciamento do Windows ADAP não pôde criar a classe de \_ base PerfRawData do Win32% 1.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ falha \_ ao \_ iniciar o repositório do WBEM MC**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



O serviço de Instrumentação de Gerenciamento do Windows falhou ao carregar os arquivos de repositório no diretório *% windir% \\ System32 \\ WBEM \\ Repository*. Isso pode ser causado por um dano nos arquivos do repositório, configurações de segurança nesse diretório, falta de espaço em disco ou outros problemas de recursos do sistema, como a falta de memória. Se esse erro ocorrer toda vez que o computador for reiniciado, o administrador neste computador poderá precisar parar o serviço WMI, examinar a configuração de segurança nessa pasta e nos arquivos dessa pasta e executar WMIDiag para validar a integridade do Instrumentação de Gerenciamento do Windows.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ requer \_ criptografia \_ negada**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



O acesso ao namespace %1 foi negado porque o namespace está marcado com RequiresEncryption, mas o script ou o aplicativo tentou se conectar a esse namespace com um nível de autenticação abaixo da **\_ privacidade do PKT**. Altere o nível de autenticação **para \_ privacidade de PKT** e execute o script ou o aplicativo novamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ requer \_ criptografia \_ assíncrona \_ negada**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



O serviço de Instrumentação de Gerenciamento do Windows não pôde entregar resultados de forma assíncrona para o namespace %1. O namespace é marcado com RequiresEncryption, mas WinMgmt não pôde estabelecer uma conexão segura de volta para o computador cliente. Verifique se há uma relação de confiança entre os computadores cliente e servidor para que o cliente reconheça a conta de computador do servidor.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**HOST do WBEM \_ MC \_ WBEM \_ \_ eliminado**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Instrumentação de Gerenciamento do Windows parou WMIPRVSE.EXE porque uma cota atingiu um valor de aviso. Cota: %1 valor: %2 valor máximo: %3 PID do WMIPRVSE: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Durante a inicialização do serviço, o serviço de Instrumentação de Gerenciamento do Windows não pôde localizar os arquivos do repositório. Um novo repositório será criado com base no mecanismo de recuperação automática.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM \_ iniciado com \_ êxito**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Instrumentação de Gerenciamento do Windows serviço foi iniciado com êxito.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM \_ principal \_ PSS \_ ESS \_ inicializado**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Instrumentação de Gerenciamento do Windows subsistemas de serviço inicializados com êxito.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_ \_ \_ \_ falha na inicialização do serviço WBEM MC WBEM \_**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



O número de erro %1 foi retornado ao tentar inicializar o serviço de Instrumentação de Gerenciamento do Windows. Isso pode ser devido a uma versão mal instalada do WMI, falha na atualização do repositório WMI, espaço em disco insuficiente ou memória insuficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**repositório do WBEM \_ MC \_ WBEM \_ \_ recriado**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



O repositório de Instrumentação de Gerenciamento do Windows recriou com êxito usando o mecanismo de recuperação automatizada.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos WMI](wmi-events.md)
</dt> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> </dl>

 

 




