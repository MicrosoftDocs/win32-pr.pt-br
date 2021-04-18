---
title: Tipo simples de privilegetype
description: Os privilégios determinam o tipo de operações do sistema que uma conta de usuário pode executar. Um administrador atribui privilégios a contas de usuário e de grupo. Os privilégios de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- tipo simples de privilegetype Agendador de Tarefas
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4864364a4752d72bd5305c5c2591b7d27391517f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781030"
---
# <a name="privilegetype-simple-type"></a>Tipo simples de privilegetype

Os privilégios determinam o tipo de operações do sistema que uma conta de usuário pode executar. Um administrador atribui privilégios a contas de usuário e de grupo. Os privilégios de cada usuário incluem aqueles concedidos ao usuário e aos grupos aos quais o usuário pertence.

``` syntax
<xs:simpleType name="privilegeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="SeCreateTokenPrivilege"
         />
        <xs:enumeration
            value="SeAssignPrimaryTokenPrivilege"
         />
        <xs:enumeration
            value="SeLockMemoryPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseQuotaPrivilege"
         />
        <xs:enumeration
            value="SeUnsolicitedInputPrivilege"
         />
        <xs:enumeration
            value="SeMachineAccountPrivilege"
         />
        <xs:enumeration
            value="SeTcbPrivilege"
         />
        <xs:enumeration
            value="SeSecurityPrivilege"
         />
        <xs:enumeration
            value="SeTakeOwnershipPrivilege"
         />
        <xs:enumeration
            value="SeLoadDriverPrivilege"
         />
        <xs:enumeration
            value="SeSystemProfilePrivilege"
         />
        <xs:enumeration
            value="SeSystemtimePrivilege"
         />
        <xs:enumeration
            value="SeProfileSingleProcessPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseBasePriorityPrivilege"
         />
        <xs:enumeration
            value="SeCreatePagefilePrivilege"
         />
        <xs:enumeration
            value="SeCreatePermanentPrivilege"
         />
        <xs:enumeration
            value="SeBackupPrivilege"
         />
        <xs:enumeration
            value="SeRestorePrivilege"
         />
        <xs:enumeration
            value="SeShutdownPrivilege"
         />
        <xs:enumeration
            value="SeDebugPrivilege"
         />
        <xs:enumeration
            value="SeAuditPrivilege"
         />
        <xs:enumeration
            value="SeSystemEnvironmentPrivilege"
         />
        <xs:enumeration
            value="SeChangeNotifyPrivilege"
         />
        <xs:enumeration
            value="SeRemoteShutdownPrivilege"
         />
        <xs:enumeration
            value="SeUndockPrivilege"
         />
        <xs:enumeration
            value="SeSyncAgentPrivilege"
         />
        <xs:enumeration
            value="SeEnableDelegationPrivilege"
         />
        <xs:enumeration
            value="SeManageVolumePrivilege"
         />
        <xs:enumeration
            value="SeImpersonatePrivilege"
         />
        <xs:enumeration
            value="SeCreateGlobalPrivilege"
         />
        <xs:enumeration
            value="SeTrustedCredManAccessPrivilege"
         />
        <xs:enumeration
            value="SeRelabelPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseWorkingSetPrivilege"
         />
        <xs:enumeration
            value="SeTimeZonePrivilege"
         />
        <xs:enumeration
            value="SeCreateSymbolicLinkPrivilege"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeração

O tipo simples **privilegetype** define os valores a seguir.



| Valor                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Necessário para criar um token primário. Direito de usuário: criar um objeto de token.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Necessário para atribuir o token primário de um processo. Direito de usuário: substituir um token de nível de processo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Necessário para bloquear páginas físicas na memória. Direito de usuário: bloquear páginas na memória. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Necessário para aumentar a cota atribuída a um processo. Direito de usuário: Ajustar cotas de memória para um processo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | Necessário para ler a entrada não solicitada de um dispositivo de terminal. Direito de usuário: não aplicável. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Necessário para criar uma conta de computador. Direito de usuário: Adicionar estações de trabalho ao domínio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege;                  | Esse privilégio identifica seu detentor como parte da base do computador confiável. Alguns subsistemas protegidos confiáveis recebem esse privilégio. Direito de usuário: agir como parte do sistema operacional. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Necessário para executar uma série de funções relacionadas à segurança, como controlar e exibir mensagens de auditoria. Esse privilégio identifica seu detentor como um operador de segurança. Direito de usuário: gerenciar a auditoria e o log de segurança. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Necessário para apropriar-se de um objeto sem ter acesso discricionário. Esse privilégio permite que o valor do proprietário seja definido somente para os valores que o detentor pode atribuir legitimamente como o proprietário de um objeto. Direito de usuário: apropriar-se de arquivos ou outros objetos. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Necessário para carregar ou descarregar um driver de dispositivo. Direito de usuário: carregar e descarregar drivers de dispositivo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Necessário para reunir informações de criação de perfil para todo o sistema. Direito do usuário: desempenho do sistema do perfil. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Necessário para modificar a hora do sistema. Direito de usuário: alterar a hora do sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Necessário para reunir informações de criação de perfil para um único processo. Direito de usuário: processo único de perfil. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Necessário para aumentar a prioridade base de um processo. Direito de usuário: aumentar a prioridade de agendamento. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Necessário para criar um arquivo de paginação. Direito de usuário: criar um arquivo de paginação. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Necessário para criar um objeto permanente. Direito de usuário: criar objetos compartilhados permanentes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Necessário para executar operações de backup. Esse privilégio faz com que o sistema conceda todo o controle de acesso de leitura a qualquer arquivo, independentemente da ACL (lista de controle de acesso) especificada para o arquivo. Qualquer solicitação de acesso diferente da leitura ainda é avaliada com a ACL. Esse privilégio é exigido pelo RegSaveKey e RegSaveKeyExfunctions. Os direitos de acesso a seguir serão concedidos se esse privilégio for mantido: \_ controle de leitura, \_ segurança do sistema \_ de acesso, \_ \_ leitura genérica de arquivo, desvio de arquivo \_ . Direito de usuário: fazer backup de arquivos e diretórios. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Necessário para executar operações de restauração. Esse privilégio faz com que o sistema conceda todo o controle de acesso de gravação a qualquer arquivo, independentemente da ACL especificada para o arquivo. Qualquer solicitação de acesso diferente da gravação ainda é avaliada com a ACL. Além disso, esse privilégio permite que você defina qualquer SID (identificador de segurança) de usuário ou grupo válido como o proprietário de um arquivo. Esse privilégio é exigido pela função RegLoadKey. Os direitos de acesso a seguir serão concedidos se esse privilégio for mantido: gravar \_ DAC, proprietário da gravação \_ , \_ segurança do sistema \_ de acesso, gravação genérica do arquivo, arquivo \_ \_ \_ Adicionar \_ arquivo, arquivo \_ Adicionar \_ subdiretório, excluir. Direito de usuário: restaurar arquivos e diretórios. <br/> |
| SeShutdownPrivilege             | Necessário para desligar um sistema local. Direito de usuário: desligar o sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Necessário para depurar e ajustar a memória de um processo de propriedade de outra conta. Direito do usuário: depurar programas. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Necessário para gerar entradas de log de auditoria. Dê esse privilégio a servidores seguros. Direito de usuário: gerar auditorias de segurança. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Necessário para modificar a RAM não volátil de sistemas que usam esse tipo de memória para armazenar informações de configuração. Direito de usuário: modificar valores de ambiente de firmware. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Necessário para receber notificações de alterações em arquivos ou diretórios. Esse privilégio também faz com que o sistema ignore todas as verificações de acesso de passagem. Ele é habilitado por padrão para todos os usuários. Direito do usuário: ignorar a verificação completa. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Necessário para desligar um sistema usando uma solicitação de rede. Direito de usuário: forçar o desligamento de um sistema remoto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Necessário para desencaixar um laptop. Direito de usuário: remover computador da estação de encaixe. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Necessário para um controlador de domínio usar os serviços de sincronização de diretório LDAP. Esse privilégio permite que o detentor Leia todos os objetos e propriedades no diretório, independentemente da proteção nos objetos e propriedades. Por padrão, ele é atribuído às contas de administrador e LocalSystem em controladores de domínio. Direito do usuário: sincronizar dados do serviço de diretório. <br/>                                                                                                                                                                                                                                                                                |
| Seenabledelegationprivilege foi     | Necessário para marcar contas de usuário e computador como confiáveis para delegação. Direito de usuário: habilitar contas de computador e de usuário para serem confiáveis para delegação. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Necessário para habilitar os privilégios de gerenciamento de volume. Direito do usuário: gerenciar os arquivos em um volume. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Necessário para representar. Direito de usuário: representar um cliente após a autenticação. Windows XP/2000: não há suporte para esse privilégio. <br/> Observe que esse valor tem suporte a partir do Windows Server 2003, do Windows XP com SP2 e do Windows 2000 com SP4.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Necessário para criar objetos de mapeamento de arquivo nomeado no namespace global durante sessões de serviços de terminal. Esse privilégio é habilitado por padrão para administradores, serviços e a conta sistema local. Direito de usuário: criar objetos globais. Windows XP/2000: não há suporte para esse privilégio. <br/> Observe que esse valor tem suporte a partir do Windows Server 2003, do Windows XP com SP2 e do Windows 2000 com SP4.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Necessário para acessar o Gerenciador de credenciais como um chamador confiável. Direito de usuário: acesse o Gerenciador de credenciais como um chamador confiável. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Necessário para modificar o nível de integridade obrigatório de um objeto. Direito de usuário: modificar um rótulo de objeto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Necessário para alocar mais memória para aplicativos que são executados no contexto de usuários. Direito de usuário: aumentar um conjunto de trabalho de processo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Necessário para ajustar o fuso horário associado ao relógio interno do computador. Direito de usuário: altere o fuso horário. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Necessário para criar um link simbólico. Direito de usuário: criar links simbólicos. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 





