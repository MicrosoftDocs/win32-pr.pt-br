---
Description: Os privilégios determinam o tipo de operações do sistema que uma conta de usuário pode executar. Um administrador atribui privilégios a contas de usuário e grupo. Os privilégios de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Constantes de privilégio (Winnt.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5da0a0e6f9ad3b0559fdf2d8e375e6d25e7d2fdf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475734"
---
# <a name="privilege-constants-authorization"></a>Constantes de privilégio (autorização)

Os privilégios determinam o tipo de operações do sistema que uma conta de usuário pode executar. Um administrador atribui privilégios a contas de usuário e grupo. Os privilégios de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.

As funções que obter e ajustar os privilégios em um [*token*](/windows/desktop/SecGloss/a-gly) de acesso usam o tipo luid (identificador exclusivo [*local)*](/windows/desktop/SecGloss/l-gly) para identificar privilégios. Use a [**função LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para determinar o [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) no sistema local que corresponde a uma constante de privilégio. Use a [**função LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) para converter um **LUID** em sua constante de cadeia de caracteres correspondente.

O sistema operacional representa um privilégio usando a cadeia de caracteres que segue "Direito do Usuário" na coluna Descrição da tabela a seguir. O sistema operacional exibe as cadeias  de caracteres corretas do usuário na coluna Política do nó Atribuição de Direitos de Usuário do snap-in MMC (Local **Security** Configurações Console de Gerenciamento Microsoft).

## <a name="example"></a>Exemplo

```cpp
BOOL EnablePrivilege()
{
    LUID PrivilegeRequired ;
    BOOL bRes = FALSE;
  
    bRes = LookupPrivilegeValue(NULL, SE_DEBUG_NAME, &PrivilegeRequired);

    // ...

    return bRes;
}
```
Exemplo de [Windows exemplos clássicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) em GitHub.

## <a name="constants"></a>Constantes



| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl><dt><strong>SE_ASSIGNPRIMARYTOKEN_NAME</strong></dt><dt>TEXT("SeAssignPrimaryTokenPrivilege")</dt></dl> | Necessário para atribuir o <a href="/windows/desktop/SecGloss/p-gly"><em>token primário</em></a> de um processo. <br /> Direito do usuário: substitua um token no nível do processo.<br /> | 
| <span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl><dt><strong>SE_AUDIT_NAME</strong></dt><dt>TEXT("SeAuditPrivilege")</dt></dl> | Necessário para gerar entradas de log de auditoria. Dê esse privilégio a servidores seguros. <br /> Direito do usuário: gerar auditorias de segurança.<br /> | 
| <span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl><dt><strong>SE_BACKUP_NAME</strong></dt><dt>TEXT("SeBackupPrivilege")</dt></dl> | Necessário para executar operações de backup. Esse privilégio faz com que o sistema conceda todo o controle de acesso de leitura a qualquer arquivo, independentemente da ACL <a href="/windows/desktop/SecGloss/a-gly"><em>(lista</em></a> de controle de acesso) especificada para o arquivo. Qualquer solicitação de acesso diferente de leitura ainda é avaliada com a ACL. Esse privilégio é exigido pelas funções <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a> e <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx.</strong></a> Os seguintes direitos de acesso serão concedidos se esse privilégio for mantido:<br /><ul><li>READ_CONTROL</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_READ</li><li>FILE_TRAVERSE</li></ul>Direito do usuário: fazer o back-up de arquivos e diretórios.<br />Se o arquivo estiver localizado em uma unidade removível e a "Auditoria Armazenamento removível" estiver habilitada, o SE_SECURITY_NAME será necessário ter ACCESS_SYSTEM_SECURITY. | 
| <span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl><dt><strong>SE_CHANGE_NOTIFY_NAME</strong></dt><dt>TEXT("SeChangeNotifyPrivilege")</dt></dl> | Necessário para receber notificações de alterações em arquivos ou diretórios. Esse privilégio também faz com que o sistema ignore todas as verificações de acesso de travessia. Ele é habilitado por padrão para todos os usuários. <br /> Direito do usuário: ignorar a verificação de travessia.<br /> | 
| <span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl><dt><strong>SE_CREATE_GLOBAL_NAME</strong></dt><dt>TEXT("SeCreateGlobalPrivilege")</dt></dl> | Necessário para criar objetos de mapeamento de arquivo nomeados no namespace global durante as sessões dos Serviços de Terminal. Esse privilégio é habilitado por padrão para administradores, serviços e a conta do sistema local.<br /> Direito do usuário: criar objetos globais.<br /> | 
| <span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl><dt><strong>SE_CREATE_PAGEFILE_NAME</strong></dt><dt>TEXT("SeCreatePagefilePrivilege")</dt></dl> | Necessário para criar um arquivo de paging. <br /> Direito do usuário: crie um arquivo de página.<br /> | 
| <span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl><dt><strong>SE_CREATE_PERMANENT_NAME</strong></dt><dt>TEXT("SeCreatePermanentPrivilege")</dt></dl> | Necessário para criar um objeto permanente. <br /> Direito do Usuário: criar objetos compartilhados permanentes.<br /> | 
| <span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl><dt><strong>SE_CREATE_SYMBOLIC_LINK_NAME</strong></dt><dt>TEXT("SeCreateSymbolicLinkPrivilege")</dt></dl> | Necessário para criar um link simbólico.<br /> Direito do usuário: criar links simbólicos.<br /> | 
| <span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl><dt><strong>SE_CREATE_TOKEN_NAME</strong></dt><dt>TEXT("SeCreateTokenPrivilege")</dt></dl> | Necessário para criar um token primário. <br /> Direito do usuário: crie um objeto de token.<br /> Não é possível adicionar esse privilégio a uma conta de usuário com a política "Criar um objeto de token". Além disso, você não pode adicionar esse privilégio a um processo de propriedade usando Windows APIs. <strong>Windows Server 2003</strong> e Windows XP com SP1 e versões anteriores: as APIs Windows podem adicionar esse privilégio a um processo de propriedade.<br /><br /> | 
| <span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl><dt><strong>SE_DEBUG_NAME</strong></dt><dt>TEXT("SeDebugPrivilege")</dt></dl> | Necessário para depurar e ajustar a memória de um processo pertencente a outra conta. <br /> Direito do usuário: depurar programas.<br /> | 
| <span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl><dt><strong>SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME</strong></dt><dt>TEXT("SeDelegateSessionUserImpersonatePrivilege")</dt></dl> | Necessário para obter um token de representação para outro usuário na mesma sessão. <br /> Direito do usuário: representar outros usuários.<br /> | 
| <span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl><dt><strong>SE_ENABLE_DELEGATION_NAME</strong></dt><dt>TEXT("SeEnableDelegationPrivilege")</dt></dl> | Necessário para marcar contas de usuário e computador como confiáveis para delegação.<br /> Direito do usuário: habilita as contas de computador e de usuário a serem confiáveis para delegação.<br /> | 
| <span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl><dt><strong>SE_IMPERSONATE_NAME</strong></dt><dt>TEXT("SeImpersonatePrivilege")</dt></dl> | Necessário para representar.<br /> Direito do usuário: representar um cliente após a autenticação.<br /> | 
| <span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl><dt><strong>SE_INC_BASE_PRIORITY_NAME</strong></dt><dt>TEXT("SeIncreaseBasePriorityPrivilege")</dt></dl> | Necessário para aumentar a prioridade base de um processo. <br /> Direito do usuário: aumentar a prioridade de agendamento.<br /> | 
| <span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl><dt><strong>SE_INCREASE_QUOTA_NAME</strong></dt><dt>TEXT("SeIncreaseQuotaPrivilege")</dt></dl> | Necessário para aumentar a cota atribuída a um processo. <br /> Direito do usuário: ajuste as cotas de memória para um processo.<br /> | 
| <span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl><dt><strong>SE_INC_WORKING_SET_NAME</strong></dt><dt>TEXT("SeIncreaseWorkingSetPrivilege")</dt></dl> | Necessário para alocar mais memória para aplicativos executados no contexto de usuários.<br /> Direito do usuário: aumente um conjunto de trabalho do processo.<br /> | 
| <span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl><dt><strong>SE_LOAD_DRIVER_NAME</strong></dt><dt>TEXT("SeLoadDriverPrivilege")</dt></dl> | Necessário para carregar ou descarregar um driver de dispositivo. <br /> Direito do usuário: carregar e descarregar drivers de dispositivo.<br /> | 
| <span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl><dt><strong>SE_LOCK_MEMORY_NAME</strong></dt><dt>TEXT("SeLockMemoryPrivilege")</dt></dl> | Necessário para bloquear páginas físicas na memória. <br /> Direito do Usuário: bloquear páginas na memória.<br /> | 
| <span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl><dt><strong>SE_MACHINE_ACCOUNT_NAME</strong></dt><dt>TEXT("SeMachineAccountPrivilege")</dt></dl> | Necessário para criar uma conta de computador. <br /> Direito do usuário: adicionar estações de trabalho ao domínio.<br /> | 
| <span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl><dt><strong>SE_MANAGE_VOLUME_NAME</strong></dt><dt>TEXT("SeManageVolumePrivilege")</dt></dl> | Necessário para habilitar privilégios de gerenciamento de volume. <br /> Direito do usuário: gerencie os arquivos em um volume.<br /> | 
| <span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl><dt><strong>SE_PROF_SINGLE_PROCESS_NAME</strong></dt><dt>TEXT("SeProfileSingleProcessPrivilege")</dt></dl> | Necessário para coletar informações de criação de perfil para um único processo. <br /> Direito do usuário: perfil de processo único.<br /> | 
| <span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl><dt><strong>SE_RELABEL_NAME</strong></dt><dt>TEXT("SeRelabelPrivilege")</dt></dl> | Necessário para modificar o nível de integridade obrigatório de um objeto .<br /> Direito do usuário: modifique um rótulo de objeto.<br /> | 
| <span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl><dt><strong>SE_REMOTE_SHUTDOWN_NAME</strong></dt><dt>TEXT("SeRemoteShutdownPrivilege")</dt></dl> | Necessário para desligar um sistema usando uma solicitação de rede. <br /> Direito de usuário: forçar o desligamento de um sistema remoto.<br /> | 
| <span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_RESTORE_NAME ("SeRestorePrivilege")</dt></dl> | Necessário para executar operações de restauração. Esse privilégio faz com que o sistema conceda todo o controle de acesso de gravação a qualquer arquivo, independentemente da ACL especificada para o arquivo. Qualquer solicitação de acesso diferente da gravação ainda é avaliada com a ACL. Além disso, esse privilégio permite que você defina qualquer SID de grupo ou usuário válido como o proprietário de um arquivo. Esse privilégio é exigido pela função <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a> . Os direitos de acesso a seguir serão concedidos se esse privilégio for mantido:<br /><ul><li>WRITE_DAC</li><li>WRITE_OWNER</li><li>ACCESS_SYSTEM_SECURITY</li><li>FILE_GENERIC_WRITE</li><li>FILE_ADD_FILE</li><li>FILE_ADD_SUBDIRECTORY</li><li>Delete (excluir)</li></ul>Direito de usuário: restaurar arquivos e diretórios.<br />se o arquivo estiver localizado em uma unidade removível e a "auditoria removível Armazenamento" estiver habilitada, o SE_SECURITY_NAME precisará ter ACCESS_SYSTEM_SECURITY.<br /> | 
| <span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl><dt><strong>SE_SECURITY_NAME</strong></dt><dt>texto ("SeSecurityPrivilege")</dt></dl> | Necessário para executar uma série de funções relacionadas à segurança, como controlar e exibir mensagens de auditoria. Esse privilégio identifica seu detentor como um operador de segurança. <br /> Direito de usuário: gerenciar auditoria e log de segurança.<br /> | 
| <span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_SHUTDOWN_NAME ("SeShutdownPrivilege")</dt></dl> | Necessário para desligar um sistema local. <br /> Direito de usuário: desligar o sistema.<br /> | 
| <span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_SYNC_AGENT_NAME ("SeSyncAgentPrivilege")</dt></dl> | Necessário para um controlador de domínio usar os serviços de sincronização de diretório do <a href="/windows/desktop/SecGloss/l-gly"><em>protocolo de acesso ao diretório Lightweight Directory</em></a> . Esse privilégio permite que o detentor Leia todos os objetos e propriedades no diretório, independentemente da proteção nos objetos e propriedades. Por padrão, ele é atribuído às contas de administrador e LocalSystem em controladores de domínio. <br /> Direito do usuário: sincronizar dados do serviço de diretório.<br /> | 
| <span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_SYSTEM_ENVIRONMENT_NAME ("SeSystemEnvironmentPrivilege")</dt></dl> | Necessário para modificar a RAM não volátil de sistemas que usam esse tipo de memória para armazenar informações de configuração. <br /> Direito de usuário: modificar valores de ambiente de firmware.<br /> | 
| <span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_SYSTEM_PROFILE_NAME ("SeSystemProfilePrivilege")</dt></dl> | Necessário para reunir informações de criação de perfil para todo o sistema. <br /> Direito do usuário: desempenho do sistema do perfil.<br /> | 
| <span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_SYSTEMTIME_NAME ("SeSystemtimePrivilege")</dt></dl> | Necessário para modificar a hora do sistema. <br /> Direito de usuário: alterar a hora do sistema.<br /> | 
| <span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_TAKE_OWNERSHIP_NAME ("SeTakeOwnershipPrivilege")</dt></dl> | Necessário para apropriar-se de um objeto sem ter acesso discricionário. Esse privilégio permite que o valor do proprietário seja definido somente para os valores que o detentor pode atribuir legitimamente como o proprietário de um objeto. <br /> Direito de usuário: apropriar-se de arquivos ou outros objetos.<br /> | 
| <span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_TCB_NAME ("SeTcbPrivilege;")</dt></dl> | Esse privilégio identifica seu detentor como parte da base do computador confiável. Alguns subsistemas protegidos confiáveis recebem esse privilégio. <br /> Direito de usuário: agir como parte do sistema operacional.<br /> | 
| <span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_TIME_ZONE_NAME ("SeTimeZonePrivilege")</dt></dl> | Necessário para ajustar o fuso horário associado ao relógio interno do computador.<br /> Direito de usuário: altere o fuso horário.<br /> | 
| <span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_TRUSTED_CREDMAN_ACCESS_NAME ("SeTrustedCredManAccessPrivilege")</dt></dl> | Necessário para acessar o Gerenciador de credenciais como um chamador confiável.<br /> Direito de usuário: acesse o Gerenciador de credenciais como um chamador confiável.<br /> | 
| <span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_UNDOCK_NAME ("SeUndockPrivilege")</dt></dl> | Necessário para desencaixar um laptop.<br /> Direito de usuário: remover computador da estação de encaixe.<br /> | 
| <span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl><dt><strong></strong></dt><dt>Texto de SE_UNSOLICITED_INPUT_NAME ("SeUnsolicitedInputPrivilege")</dt></dl> | Necessário para ler a entrada não solicitada de um dispositivo de <a href="/windows/desktop/SecGloss/t-gly"><em>terminal</em></a> .<br /> Direito de usuário: não aplicável.<br /> | 




## <a name="remarks"></a>Comentários

As constantes de privilégio são definidas como cadeias de caracteres em Winnt. h. por exemplo, a \_ constante de nome de auditoria ES \_ é definida como "SeAuditPrivilege".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Privilégios](privileges.md)
</dt> </dl>

