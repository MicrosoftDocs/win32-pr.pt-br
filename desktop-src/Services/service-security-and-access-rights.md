---
description: O modelo de segurança do Windows permite controlar o acesso ao SCM (Gerenciador de controle de serviço) e aos objetos de serviço.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Segurança do serviço e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769185"
---
# <a name="service-security-and-access-rights"></a>Segurança do serviço e direitos de acesso

O modelo de segurança do Windows permite controlar o acesso ao SCM (Gerenciador de controle de serviço) e aos objetos de serviço. As seções a seguir fornecem informações detalhadas:

-   [Direitos de acesso para o Gerenciador de controle de serviço](#access-rights-for-the-service-control-manager)
-   [Direitos de acesso para um serviço](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>Direitos de acesso para o Gerenciador de controle de serviço

A seguir estão os direitos de acesso específicos para o SCM.



| Direito de acesso                                   | Descrição                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sc \_ MANAGER \_ All \_ Access** (0xF003F)         | Inclui **\_ direitos padrão \_ necessários**, além de todos os direitos de acesso nesta tabela.                                                                                                                                                                                                                                                                                 |
| **Sc \_ \_ \_ Serviço de criação do Gerenciador** (0x0002)      | Necessário para chamar a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para criar um objeto de serviço e adicioná-lo ao banco de dados.                                                                                                                                                                                                                                              |
| **Sc \_ \_Conexão do Gerenciador** (0x0001)              | Necessário para se conectar ao Gerenciador de controle de serviço.                                                                                                                                                                                                                                                                                                                      |
| **Sc \_ \_ \_ Serviço de enumeração do Gerenciador** (0x0004)   | Necessário para chamar a função [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) ou [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para listar os serviços que estão no banco de dados.<br/> Necessário para chamar a função [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para receber notificação quando qualquer serviço for criado ou excluído.<br/> |
| **Sc \_ \_Bloqueio do Gerenciador** (0x0008)                 | Necessário para chamar a função [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) para adquirir um bloqueio no banco de dados.                                                                                                                                                                                                                                                      |
| **Sc \_ MANAGER \_ Modify \_ \_ config boot** (0x0020) | Necessário para chamar a função [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .                                                                                                                                                                                                                                                                                  |
| **Sc \_ \_Status de \_ bloqueio \_ de consulta do Gerenciador** (0x0010)  | Necessário para chamar a função [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) para recuperar as informações de status de bloqueio do banco de dados.                                                                                                                                                                                                                         |



 

A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para o SCM.



<table>
<thead>
<tr class="header">
<th>Direito de acesso</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SC_MANAGER_CREATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_LOCK</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_ALL</strong></td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Um processo com os direitos de acesso corretos pode abrir um identificador para o SCM que pode ser usado nas funções [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)e [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) . Somente processos com privilégios de administrador são capazes de abrir identificadores para o SCM que pode ser usado pelas funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .

O sistema cria o descritor de segurança para o SCM. Para obter ou definir o descritor de segurança para o SCM, use as funções [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) com um identificador para o objeto SCManager.

**Windows Server 2003 e Windows XP:** Ao contrário da maioria dos outros objetos protegíveis, o descritor de segurança para o SCM não pode ser modificado. Esse comportamento foi alterado a partir do Windows Server 2003 com Service Pack 1 (SP1).

Os direitos de acesso a seguir são concedidos.



<table>
<thead>
<tr class="header">
<th>Conta</th>
<th>Direitos de acesso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Usuários autenticados remotamente</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Usuários autenticados locais (incluindo LocalService e NetworkService)</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administradores</td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Observe que os usuários remotos autenticados pela rede, mas não conectados interativamente, podem se conectar ao SCM, mas não executar operações que exigem outros direitos de acesso. Para executar essas operações, o usuário deve fazer logon interativamente ou o serviço deve usar uma das contas de serviço.

**Windows Server 2003 e Windows XP:** Os usuários remotos autenticados recebem o serviço de enumeração SC Manager **\_ \_ Connect**, **sc \_ Manager \_ \_**, o **status de bloqueio de \_ \_ consulta SC \_ \_ Manager** e direitos padrão de acesso de **\_ \_ leitura de direitos** . Esses direitos de acesso são restritos conforme descrito na tabela anterior a partir do Windows Server 2003 com SP1

Quando um processo usa a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para abrir um identificador para um banco de dados de serviços instalados, ele pode solicitar direitos de acesso. O sistema executa uma verificação de segurança no descritor de segurança do SCM antes de conceder os direitos de acesso solicitados.

## <a name="access-rights-for-a-service"></a>Direitos de acesso para um serviço

A seguir estão os direitos de acesso específicos para um serviço.



| Direito de acesso                                | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Serviço \_ do Todos os \_ acessos** (0xF01FF)          | Inclui **\_ direitos padrão \_ necessários** além de todos os direitos de acesso nesta tabela.                                                                                                                                                                                                                                                                                              |
| **Serviço \_ do ALTERAR \_ configuração** (0x0002)        | Necessário para chamar a função [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) para alterar a configuração do serviço. Como isso concede ao chamador o direito de alterar o arquivo executável que o sistema executa, ele deve ser concedido somente aos administradores.                                                              |
| **Serviço \_ do ENUMERAr \_ dependentes** (0x0008) | Necessário para chamar a função [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar todos os serviços dependentes do serviço.                                                                                                                                                                                                                                         |
| **Serviço \_ do INTERROGAte** (0x0080)           | Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para solicitar que o serviço relate seu status imediatamente.                                                                                                                                                                                                                                                          |
| **Serviço \_ do Pausar \_ continuar** (0x0040)       | Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pausar ou continuar o serviço.                                                                                                                                                                                                                                                                             |
| **Serviço \_ do \_Configuração de consulta** (0x0001)         | Necessário para chamar as funções [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para consultar a configuração do serviço.                                                                                                                                                                                                           |
| **Serviço \_ do \_Status da consulta** (0x0004)         | Necessário para chamar a função [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) ou [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para perguntar ao Gerenciador de controle de serviço sobre o status do serviço.<br/> Necessário para chamar a função [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para receber notificação quando um serviço altera o status.<br/> |
| **Serviço \_ do Iniciar** (0x0010)                 | Necessário para chamar a função [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para iniciar o serviço.                                                                                                                                                                                                                                                                                             |
| **Serviço \_ do PARAR** (0x0020)                  | Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para interromper o serviço.                                                                                                                                                                                                                                                                                          |
| **Serviço \_ do \_ \_ Controle definido pelo usuário**(0x0100) | Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para especificar um código de controle definido pelo usuário.                                                                                                                                                                                                                                                                       |



 

A seguir estão os [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) para um serviço.



| Direito de acesso                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_segurança do sistema de acesso \_** | Necessário para chamar a função [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) ou [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para acessar a SACL. A maneira apropriada de obter esse acesso é habilitar o [**privilégio**](/windows/desktop/SecAuthZ/privileges) **\_ \_ nome de segurança se** no token de acesso atual do chamador, abrir o identificador para acessar acesso à **\_ \_ segurança do sistema** e, em seguida, desabilitar o privilégio. |
| **Excluir**   (0x10000)       | Necessário para chamar a função [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para excluir o serviço.                                                                                                                                                                                                                                                                                                                                                  |
| **Ler \_ CONTROL**  (0x20000)    | Necessário para chamar a função [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) para consultar o descritor de segurança do objeto de serviço.                                                                                                                                                                                                                                                                                  |
| **Gravar \_ DAC**  (0x40000)    | Necessário para chamar a função [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar o membro **DACL** do descritor de segurança do objeto de serviço.                                                                                                                                                                                                                                                                   |
| **Gravar \_ PROPRIETÁRIO** (0x80000)   | Necessário para chamar a função [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar o **proprietário** e os membros do **grupo** do descritor de segurança do objeto de serviço.                                                                                                                                                                                                                                                   |



 

A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para um serviço.



<table>
<thead>
<tr class="header">
<th>Direito de acesso</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SERVICE_CHANGE_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

O SCM cria um descritor de segurança do objeto de serviço quando o serviço é instalado pela função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) . O descritor de segurança padrão de um objeto de serviço concede o acesso a seguir.



<table>
<thead>
<tr class="header">
<th>Conta</th>
<th>Direitos de acesso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Usuários autenticados remotamente</td>
<td>Não concedido por padrão. <strong>Windows Server 2003 com SP1: SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 e Windows XP:</strong> Os direitos de acesso para usuários autenticados remotos são os mesmos para usuários autenticados locais.<br/></td>
</tr>
<tr class="even">
<td>Usuários autenticados locais (incluindo LocalService e NetworkService)</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administradores</td>
<td><dl> <strong>DELETE</strong><br />
<strong>READ_CONTROL</strong><br />
<strong>SERVICE_ALL_ACCESS</strong><br />
<strong>WRITE_DAC</strong><br />
<strong>WRITE_OWNER</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Para executar qualquer operação, o usuário deve fazer logon interativamente ou o serviço deve usar uma das contas de serviço.

Para obter ou definir o descritor de segurança para um objeto de serviço, use as funções [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Para obter mais informações, consulte [modificando a DACL de um serviço](modifying-the-dacl-for-a-service.md).

Quando um processo usa a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança do objeto de serviço.

A concessão de determinados direitos de acesso a usuários não confiáveis (como **\_ \_ configuração de alteração de serviço** ou **\_ parada de serviço**) pode permitir que eles interfiram na execução do serviço e, possivelmente, permitir que eles executem aplicativos na conta LocalSystem.

Quando a [**função EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) for chamada, se o chamador não tiver o direito de acesso de **status de \_ consulta \_ de serviço** a um serviço, o serviço será silenciosamente omitido da lista de serviços retornada ao cliente.

 

