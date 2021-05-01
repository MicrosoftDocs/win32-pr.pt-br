---
Description: Os privilégios determinam o tipo de operações do sistema que uma conta de usuário pode executar. Um administrador atribui privilégios a contas de usuário e de grupo. Os privilégios de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.
ms.assetid: 973796a6-bc2e-4e64-92db-5e17b9c25460
title: Constantes de privilégio (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: cd33cf947f6425d717b4d41524fe7cf0fed14cef
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327151"
---
# <a name="privilege-constants-authorization"></a>Constantes de privilégio (autorização)

Os privilégios determinam o tipo de operações do sistema que uma conta de usuário pode executar. Um administrador atribui privilégios a contas de usuário e de grupo. Os privilégios de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.

As funções que obtêm e ajustam os privilégios em um [*token de acesso*](/windows/desktop/SecGloss/a-gly) usam o tipo de [*identificador local exclusivo*](/windows/desktop/SecGloss/l-gly) (LUID) para identificar os privilégios. Use a função [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para determinar o [**LUID**](/windows/desktop/api/Winnt/ns-winnt-luid) no sistema local que corresponde a uma constante de privilégio. Use a função [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) para converter um **LUID** em sua constante de cadeia de caracteres correspondente.

O sistema operacional representa um privilégio usando a cadeia de caracteres que segue "direito de usuário" na coluna Descrição da tabela a seguir. O sistema operacional exibe as cadeias de caracteres de direito de usuário na coluna **política** do nó **atribuição de direitos de usuário** do snap-in de configurações de segurança local do MMC (console de gerenciamento Microsoft).

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
Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/ManagementInfrastructure/cpp/Process/Provider/WindowsProcess.c) no github.

## <a name="constants"></a>Constantes


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valor</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SE_ASSIGNPRIMARYTOKEN_NAME"></span><span id="se_assignprimarytoken_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_ASSIGNPRIMARYTOKEN_NAME ( &quot; SeAssignPrimaryTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para atribuir o <a href="/windows/desktop/SecGloss/p-gly"><em>token primário</em></a> de um processo. <br/> Direito de usuário: substituir um token de nível de processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_AUDIT_NAME"></span><span id="se_audit_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_AUDIT_NAME ( &quot; SeAuditPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para gerar entradas de log de auditoria. Dê esse privilégio a servidores seguros. <br/> Direito de usuário: gerar auditorias de segurança.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_BACKUP_NAME"></span><span id="se_backup_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_BACKUP_NAME ( &quot; SeBackupPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para executar operações de backup. Esse privilégio faz com que o sistema conceda todo o controle de acesso de leitura a qualquer arquivo, independentemente da ACL ( <a href="/windows/desktop/SecGloss/a-gly"><em>lista de controle de acesso</em></a> ) especificada para o arquivo. Qualquer solicitação de acesso diferente da leitura ainda é avaliada com a ACL. Esse privilégio é exigido pelas funções <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeya"><strong>RegSaveKey</strong></a> e <a href="/windows/desktop/api/winreg/nf-winreg-regsavekeyexa"><strong>RegSaveKeyEx</strong></a>. Os direitos de acesso a seguir serão concedidos se esse privilégio for mantido:<br/>
<ul>
<li>READ_CONTROL</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_READ</li>
<li>FILE_TRAVERSE</li>
</ul>
Direito de usuário: fazer backup de arquivos e diretórios.<br/>Se o arquivo estiver localizado em uma unidade removível e o "auditoria removível Storage" estiver habilitado, o SE_SECURITY_NAME precisará ter ACCESS_SYSTEM_SECURITY.</td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CHANGE_NOTIFY_NAME"></span><span id="se_change_notify_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_CHANGE_NOTIFY_NAME ( &quot; SeChangeNotifyPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para receber notificações de alterações em arquivos ou diretórios. Esse privilégio também faz com que o sistema ignore todas as verificações de acesso de passagem. Ele é habilitado por padrão para todos os usuários. <br/> Direito do usuário: ignorar a verificação completa.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_GLOBAL_NAME"></span><span id="se_create_global_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_CREATE_GLOBAL_NAME ( &quot; SeCreateGlobalPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para criar objetos de mapeamento de arquivo nomeado no namespace global durante sessões de serviços de terminal. Esse privilégio é habilitado por padrão para administradores, serviços e a conta sistema local.<br/> Direito de usuário: criar objetos globais.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_PAGEFILE_NAME"></span><span id="se_create_pagefile_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_CREATE_PAGEFILE_NAME ( &quot; SeCreatePagefilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para criar um arquivo de paginação. <br/> Direito de usuário: criar um arquivo de paginação.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_PERMANENT_NAME"></span><span id="se_create_permanent_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_CREATE_PERMANENT_NAME ( &quot; SeCreatePermanentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para criar um objeto permanente. <br/> Direito de usuário: criar objetos compartilhados permanentes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_CREATE_SYMBOLIC_LINK_NAME"></span><span id="se_create_symbolic_link_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_CREATE_SYMBOLIC_LINK_NAME ( &quot; SeCreateSymbolicLinkPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para criar um link simbólico.<br/> Direito de usuário: criar links simbólicos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_CREATE_TOKEN_NAME"></span><span id="se_create_token_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_CREATE_TOKEN_NAME ( &quot; SeCreateTokenPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para criar um token primário. <br/> Direito de usuário: criar um objeto de token.<br/> Você não pode adicionar esse privilégio a uma conta de usuário com a &quot; política criar um objeto de token &quot; . Além disso, você não pode adicionar esse privilégio a um processo de propriedade usando APIs do Windows. <strong>Windows Server 2003 e Windows XP com SP1 e anterior:</strong> As APIs do Windows podem adicionar esse privilégio a um processo de propriedade.<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_DEBUG_NAME"></span><span id="se_debug_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_DEBUG_NAME ( &quot; SeDebugPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para depurar e ajustar a memória de um processo de propriedade de outra conta. <br/> Direito do usuário: depurar programas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME"></span><span id="se_delegate_session_user_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_DELEGATE_SESSION_USER_IMPERSONATE_NAME ( &quot; SeDelegateSessionUserImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para obter um token de representação para outro usuário na mesma sessão. <br/> Direito de usuário: representar outros usuários.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_ENABLE_DELEGATION_NAME"></span><span id="se_enable_delegation_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_ENABLE_DELEGATION_NAME ( &quot; seenabledelegationprivilege foi &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para marcar contas de usuário e computador como confiáveis para delegação.<br/> Direito de usuário: habilitar contas de computador e de usuário para serem confiáveis para delegação.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_IMPERSONATE_NAME"></span><span id="se_impersonate_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_IMPERSONATE_NAME ( &quot; SeImpersonatePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para representar.<br/> Direito de usuário: representar um cliente após a autenticação.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_BASE_PRIORITY_NAME"></span><span id="se_inc_base_priority_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_INC_BASE_PRIORITY_NAME ( &quot; SeIncreaseBasePriorityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para aumentar a prioridade base de um processo. <br/> Direito de usuário: aumentar a prioridade de agendamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_INCREASE_QUOTA_NAME"></span><span id="se_increase_quota_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_INCREASE_QUOTA_NAME ( &quot; SeIncreaseQuotaPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para aumentar a cota atribuída a um processo. <br/> Direito de usuário: Ajustar cotas de memória para um processo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_INC_WORKING_SET_NAME"></span><span id="se_inc_working_set_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_INC_WORKING_SET_NAME ( &quot; SeIncreaseWorkingSetPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para alocar mais memória para aplicativos que são executados no contexto de usuários.<br/> Direito de usuário: aumentar um conjunto de trabalho de processo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_LOAD_DRIVER_NAME"></span><span id="se_load_driver_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_LOAD_DRIVER_NAME ( &quot; SeLoadDriverPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para carregar ou descarregar um driver de dispositivo. <br/> Direito de usuário: carregar e descarregar drivers de dispositivo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_LOCK_MEMORY_NAME"></span><span id="se_lock_memory_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_LOCK_MEMORY_NAME ( &quot; SeLockMemoryPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para bloquear páginas físicas na memória. <br/> Direito de usuário: bloquear páginas na memória.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_MACHINE_ACCOUNT_NAME"></span><span id="se_machine_account_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_MACHINE_ACCOUNT_NAME ( &quot; SeMachineAccountPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para criar uma conta de computador. <br/> Direito de usuário: Adicionar estações de trabalho ao domínio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_MANAGE_VOLUME_NAME"></span><span id="se_manage_volume_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_MANAGE_VOLUME_NAME ( &quot; SeManageVolumePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para habilitar os privilégios de gerenciamento de volume. <br/> Direito do usuário: gerenciar os arquivos em um volume.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_PROF_SINGLE_PROCESS_NAME"></span><span id="se_prof_single_process_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_PROF_SINGLE_PROCESS_NAME ( &quot; SeProfileSingleProcessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para reunir informações de criação de perfil para um único processo. <br/> Direito de usuário: processo único de perfil.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RELABEL_NAME"></span><span id="se_relabel_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_RELABEL_NAME ( &quot; SeRelabelPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para modificar o nível de integridade obrigatório de um objeto.<br/> Direito de usuário: modificar um rótulo de objeto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_REMOTE_SHUTDOWN_NAME"></span><span id="se_remote_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_REMOTE_SHUTDOWN_NAME ( &quot; SeRemoteShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para desligar um sistema usando uma solicitação de rede. <br/> Direito de usuário: forçar o desligamento de um sistema remoto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_RESTORE_NAME"></span><span id="se_restore_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_RESTORE_NAME ( &quot; SeRestorePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para executar operações de restauração. Esse privilégio faz com que o sistema conceda todo o controle de acesso de gravação a qualquer arquivo, independentemente da ACL especificada para o arquivo. Qualquer solicitação de acesso diferente da gravação ainda é avaliada com a ACL. Além disso, esse privilégio permite que você defina qualquer SID de grupo ou usuário válido como o proprietário de um arquivo. Esse privilégio é exigido pela função <a href="/windows/desktop/api/winreg/nf-winreg-regloadkeya"><strong>RegLoadKey</strong></a> . Os direitos de acesso a seguir serão concedidos se esse privilégio for mantido:<br/>
<ul>
<li>WRITE_DAC</li>
<li>WRITE_OWNER</li>
<li>ACCESS_SYSTEM_SECURITY</li>
<li>FILE_GENERIC_WRITE</li>
<li>FILE_ADD_FILE</li>
<li>FILE_ADD_SUBDIRECTORY</li>
<li>Delete (excluir)</li>
</ul>
Direito de usuário: restaurar arquivos e diretórios.<br/>Se o arquivo estiver localizado em uma unidade removível e o "auditoria removível Storage" estiver habilitado, o SE_SECURITY_NAME precisará ter ACCESS_SYSTEM_SECURITY.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SECURITY_NAME"></span><span id="se_security_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_SECURITY_NAME ( &quot; SeSecurityPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para executar uma série de funções relacionadas à segurança, como controlar e exibir mensagens de auditoria. Esse privilégio identifica seu detentor como um operador de segurança. <br/> Direito de usuário: gerenciar auditoria e log de segurança.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SHUTDOWN_NAME"></span><span id="se_shutdown_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_SHUTDOWN_NAME ( &quot; SeShutdownPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para desligar um sistema local. <br/> Direito de usuário: desligar o sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYNC_AGENT_NAME"></span><span id="se_sync_agent_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_SYNC_AGENT_NAME ( &quot; SeSyncAgentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para um controlador de domínio usar os serviços de sincronização de diretório do <a href="/windows/desktop/SecGloss/l-gly"><em>protocolo de acesso ao diretório Lightweight Directory</em></a> . Esse privilégio permite que o detentor Leia todos os objetos e propriedades no diretório, independentemente da proteção nos objetos e propriedades. Por padrão, ele é atribuído às contas de administrador e LocalSystem em controladores de domínio. <br/> Direito do usuário: sincronizar dados do serviço de diretório.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEM_ENVIRONMENT_NAME"></span><span id="se_system_environment_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_SYSTEM_ENVIRONMENT_NAME ( &quot; SeSystemEnvironmentPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para modificar a RAM não volátil de sistemas que usam esse tipo de memória para armazenar informações de configuração. <br/> Direito de usuário: modificar valores de ambiente de firmware.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_SYSTEM_PROFILE_NAME"></span><span id="se_system_profile_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_SYSTEM_PROFILE_NAME ( &quot; SeSystemProfilePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para reunir informações de criação de perfil para todo o sistema. <br/> Direito do usuário: desempenho do sistema do perfil.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_SYSTEMTIME_NAME"></span><span id="se_systemtime_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_SYSTEMTIME_NAME ( &quot; SeSystemtimePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para modificar a hora do sistema. <br/> Direito de usuário: alterar a hora do sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TAKE_OWNERSHIP_NAME"></span><span id="se_take_ownership_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_TAKE_OWNERSHIP_NAME ( &quot; SeTakeOwnershipPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para apropriar-se de um objeto sem ter acesso discricionário. Esse privilégio permite que o valor do proprietário seja definido somente para os valores que o detentor pode atribuir legitimamente como o proprietário de um objeto. <br/> Direito de usuário: apropriar-se de arquivos ou outros objetos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TCB_NAME"></span><span id="se_tcb_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_TCB_NAME ( &quot; SeTcbPrivilege; &quot; )</dt> </dl></td>
<td style="text-align: left;">Esse privilégio identifica seu detentor como parte da base do computador confiável. Alguns subsistemas protegidos confiáveis recebem esse privilégio. <br/> Direito de usuário: agir como parte do sistema operacional.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_TIME_ZONE_NAME"></span><span id="se_time_zone_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_TIME_ZONE_NAME ( &quot; SeTimeZonePrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para ajustar o fuso horário associado ao relógio interno do computador.<br/> Direito de usuário: altere o fuso horário.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_TRUSTED_CREDMAN_ACCESS_NAME"></span><span id="se_trusted_credman_access_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_TRUSTED_CREDMAN_ACCESS_NAME ( &quot; SeTrustedCredManAccessPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para acessar o Gerenciador de credenciais como um chamador confiável.<br/> Direito de usuário: acesse o Gerenciador de credenciais como um chamador confiável.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SE_UNDOCK_NAME"></span><span id="se_undock_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_UNDOCK_NAME ( &quot; SeUndockPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para desencaixar um laptop.<br/> Direito de usuário: remover computador da estação de encaixe.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SE_UNSOLICITED_INPUT_NAME"></span><span id="se_unsolicited_input_name"></span><dl> <dt><strong></strong></dt> <dt>Texto de SE_UNSOLICITED_INPUT_NAME ( &quot; SeUnsolicitedInputPrivilege &quot; )</dt> </dl></td>
<td style="text-align: left;">Necessário para ler a entrada não solicitada de um dispositivo de <a href="/windows/desktop/SecGloss/t-gly"><em>terminal</em></a> .<br/> Direito de usuário: não aplicável.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

As constantes de privilégio são definidas como cadeias de caracteres em Winnt. h. Por exemplo, a \_ constante de nome de auditoria se \_ é definida como "SeAuditPrivilege".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Direitos](privileges.md)
</dt> </dl>

