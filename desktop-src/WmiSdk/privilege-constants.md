---
description: O parâmetro strPrivilege do método SWbemPrivilegeSet. AddAsString e o parâmetro iPrivilege para SWbemPrivilegeSet. Add exigem cadeias de caracteres de privilégio de WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Constantes de privilégio (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663244"
---
# <a name="privilege-constants"></a>Constantes de privilégio

O parâmetro *strPrivilege* do método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) e o parâmetro *iPrivilege* para [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) exigem cadeias de caracteres de privilégio de [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). Para obter mais informações sobre como usar constantes de privilégio, consulte [executando operações privilegiadas](executing-privileged-operations.md).

As constantes a seguir são definidas em [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum). A lista a seguir inclui as constantes equivalentes para C++ e cadeias de caracteres para scripts. Para formar o nome curto do script, remova o "se" e o "privilégio" do nome da constante do C++.

O exemplo de código VBScript a seguir mostra como habilitar o privilégio RemoteShutdown em um script.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



Muitos métodos WMI exigem que uma ou mais permissões sejam habilitadas. Se uma conta não tiver recebido um privilégio, ela não poderá ser habilitada para a chamada de método.

<dl> <dt>

<span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Constante de C++: se criar cadeia de caracteres  de **\_ \_ \_ nome de token** : SeCreateTokenPrivilege

Nome curto do script: **Createtoken**

Necessário para criar um objeto de token primário.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Constante de C++: **SeAssignPrimaryTokenPrivilege** String: **SeAssignPrimaryTokenPrivilege**

Nome curto de script: **AssignPrimaryToken**

Necessário para substituir um token de nível de processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Constante de C++: cadeia de **nome da memória de bloqueio do se \_ \_ \_** : **SeLockMemoryPrivilege**

Nome curto de script: **LockMemory**

Necessário para bloquear páginas na memória.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Constante de C++: se aumentar a cadeia de  caracteres do **\_ \_ \_ nome da cota** : SeIncreaseQuotaPrivilege

Nome curto de script: **IncreaseQuotaPrivilege**

Necessário para ajustar as cotas de memória de um processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Constante de C++ **: \_ máquina \_ \_ nome da conta de se** cadeia de caracteres: **SeMachineAccountPrivilege**

Nome curto de script: **MachineAccount**

Necessário para adicionar estações de trabalho a um domínio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



C Constant: **se \_ o \_ nome do TCB** String: **SeTcbPrivilege;**

Nome curto do script: **TCB**

Necessário para atuar como parte do sistema operacional. O detentor é parte da base de computadores confiáveis.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Constante de C++: cadeia de **\_ \_ nome de segurança se** : **SeSecurityPrivilege**

Nome curto do script: **segurança**

Necessário para gerenciar a auditoria e o log de segurança do NT.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Constante de C++: se obter cadeia de caracteres  de **\_ \_ \_ nome de propriedade** : SeTakeOwnershipPrivilege

Nome curto de script: **TakeOwnership**

Necessário para assumir a propriedade de arquivos ou outros objetos sem ter uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na DACL (lista de controle de *acesso discricionário* ).


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Constante de C++: se carregar cadeia de caracteres de **\_ \_ Driver** : **SeLoadDriverPrivilege**

Nome curto da script: **LoadDriver**

Necessário para carregar ou descarregar um driver de dispositivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Constante de C++: **nome do perfil do sistema se cadeia de caracteres do \_ \_ \_ Name** : **SeSystemProfilePrivilege**

Nome curto de script: **SystemProfile**

Necessário para coletar informações de perfil sobre o desempenho do sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Constante de C++: **se \_ SYSTEMTIME** \_ nome cadeia de caracteres: **SeSystemtimePrivilege**

Nome curto de script: **SYSTEMTIME**

Necessário para alterar a hora do sistema.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Constante do C++: **se Prof cadeia de \_ \_ \_ \_ nome de processo único** : **SeProfileSingleProcessPrivilege**

Nome curto de script: **ProfileSingleProcess**

Necessário para coletar informações de perfil para um único processo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Constante de C++: de **\_ \_ \_ \_ nome de prioridade base do se Inc** : **SeIncreaseBasePriorityPrivilege**

Nome curto de script: **IncreaseBasePriority**

Necessário para aumentar a prioridade de agendamento.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Constante C++: **se \_ criar \_ \_ nome de arquivo de paginação** cadeia de caracteres: **SeCreatePagefilePrivilege**

Nome curto de script: **CreatePageFile**

Necessário para criar um arquivo de paginação.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Constante de C++: **se criar cadeia de \_ \_ \_ nome permanente** : **SeCreatePermanentPrivilege**

Nome curto de script: **Createpermanent**

Necessário para criar objetos compartilhados permanentes.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Constante de C++ **: \_ se \_ nome de backup** cadeia de caracteres: **SeBackupPrivilege**

Nome curto do script: **backup**

Necessário para fazer backup de arquivos e diretórios, independentemente da ACL especificada para o arquivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Constante de C++ **: \_ se \_ nome de restauração** da cadeia de caracteres: **SeRestorePrivilege**

Nome curto da script: **restaurar**

Necessário para restaurar arquivos e diretórios, independentemente da ACL especificada para o arquivo.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Constante C++: **se \_ \_ nome do desligamento** da cadeia de caracteres: **SeShutdownPrivilege**

Nome curto do script: **desligamento**

Necessário para desligar o sistema local.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Constante de C++ **: \_ se \_ nome de depuração** cadeia de caracteres: **SeDebugPrivilege**

Nome curto do script: **depuração**

Necessário para depurar e ajustar a memória de um processo de propriedade de outra conta.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Constante de C++ **: \_ se \_ nome de auditoria** String: **SeAuditPrivilege**

Nome curto da script: **auditoria**

Necessário para gerar entradas de auditoria no log de segurança do NT. Somente servidores seguros devem ter esse privilégio.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Constante de C++: cadeia de **nome de \_ ambiente de sistema \_ \_ se** : **SeSystemEnvironmentPrivilege**

Nome curto de script: **SystemEnvironment**

Necessário para modificar a RAM não volátil de sistemas que usam esse tipo de memória para armazenar dados de configuração.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Constante de C++: **se alterar String de \_ \_ \_ nome de notificação** : **SeChangeNotifyPrivilege**

Nome curto de script: **ChangeNotify**

Necessário para receber notificações de alterações em arquivos ou diretórios e ignorar verificações de acesso de passagem. Esse privilégio é habilitado por padrão para todos os usuários.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Constante de C++: se a cadeia de **\_ \_ \_ nome de desligamento remoto** : **SeRemoteShutdownPrivilege**

Nome curto de script: **RemoteShutdown**

Necessário para desligar um computador remoto.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



C Constant: **se \_ \_ desencaixar** cadeia de caracteres de nome: **SeUndockPrivilege**

Nome curto do script: **desencaixar**

Necessário para remover um laptop de uma estação de encaixe.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Constante de C++ **: \_ se \_ \_ nome do agente de sincronização** cadeia de caracteres: **SeSyncAgentPrivilege**

Nome curto de script: **SyncAgent**

Necessário para sincronizar os dados do serviço de diretório.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Constante de C++: se habilitar a cadeia de  **\_ \_ \_ nome de delegação** : seenabledelegationprivilege foi

Nome curto de script: **EnableDelegation**

Necessário para permitir que contas de computador e de usuário sejam confiáveis para delegação.


</dt> </dl> </dd> <dt>

<span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Constante de C++: se gerenciar a cadeia de  caracteres do **\_ \_ \_ nome do volume** : SeManageVolumePrivilege

Nome curto de script: **ManageVolume**

Necessário para executar tarefas de manutenção de volume.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de API de script](scripting-api-constants.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

