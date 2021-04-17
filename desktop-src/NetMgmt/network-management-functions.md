---
title: Funções de gerenciamento de rede
description: As funções de gerenciamento de rede podem ser agrupadas da seguinte maneira.
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a169d097fbe86c95aa9aa3120c3f732a8edd2c0
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "105813135"
---
# <a name="network-management-functions"></a>Funções de gerenciamento de rede

As funções de gerenciamento de rede podem ser agrupadas da seguinte maneira.

## <a name="alert-functions"></a>Funções de alerta



| Função                                   | Descrição                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica todos os clientes registrados que um evento específico ocorreu.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Simplifica a notificação de clientes registrados de que um evento específico ocorreu, porque, ao contrário de **NetAlertRaise**, **NetAlertRaiseEx** não requer uma estrutura de [**\_ alerta padrão**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) . |



 

## <a name="api-buffer-functions"></a>Funções de buffer de API



| Função                                                 | Descrição                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Aloca memória a partir do heap. Chame essa função quando precisar de compatibilidade com a função **NetApiBufferFree** . |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera a memória alocada pela função **NetApiBufferAllocate** e outras funções de gerenciamento de rede.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Altera o tamanho de um buffer alocado por uma chamada para a função **NetApiBufferAllocate** .                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Retorna o tamanho, em bytes, de um buffer alocado por uma chamada para a função **NetApiBufferAllocate** .                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Azure Active Directory funções de informações de junção



| Função                                                       | Descrição                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetFreeAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | Libera a memória alocada para a estrutura [**de \_ \_ informações de junção DSREG**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) especificada, que contém informações de junção para um locatário e que você recuperou chamando a função [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) . |
| [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | Recupera as informações de junção para o locatário especificado. Essa função examina as informações de junção de Microsoft Azure Active Directory e a conta de trabalho que o usuário atual adicionou.                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>Serviço de diretório e funções de ingresso no domínio



| Função                                                                             | Descrição                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | Adiciona um nome alternativo para o computador especificado.                                                                                                                                                                                                                      |
| [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | Provisiona uma conta de computador para uso posterior em uma operação de ingresso no domínio offline.                                                                                                                                                                                        |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | Enumera nomes para o computador especificado.                                                                                                                                                                                                                            |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | Recupera uma lista de UOs (unidades organizacionais) nas quais uma conta de computador pode ser criada.                                                                                                                                                                              |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | Recupera informações de status de junção para o computador especificado.                                                                                                                                                                                                           |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | Une um computador a um grupo de trabalho ou domínio.                                                                                                                                                                                                                              |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | Provisiona uma conta de computador para uso posterior em uma operação de ingresso no domínio offline.                                                                                                                                                                                       |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | Remove um nome alternativo para o computador especificado.                                                                                                                                                                                                                   |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | Altera o nome de um computador em um domínio.                                                                                                                                                                                                                             |
| [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | Executa localmente em um computador para modificar uma imagem do sistema operacional Windows montada em um volume. O registro é carregado para a imagem e os dados de blob de provisionamento são gravados onde podem ser recuperados durante a fase de conclusão de uma operação de ingresso no domínio offline.     |
| [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | Executa localmente em um computador para modificar uma imagem do sistema operacional Windows montada em um volume. O registro é carregado da imagem e os dados do pacote de provisionamento são gravados onde podem ser recuperados durante a fase de conclusão de uma operação de ingresso no domínio offline. |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | Define o nome do computador primário para o computador especificado.                                                                                                                                                                                                              |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Desassocia um computador de um grupo de trabalho ou domínio.                                                                                                                                                                                                                        |
| [**Netvalidaname**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | Verifica a validade de um nome de computador, nome de grupo de trabalho ou nome de domínio.                                                                                                                                                                                               |



 

## <a name="get-functions"></a>Obter funções



| Função                                                               | Descrição                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Retorna o nome de qualquer controlador de domínio para um domínio que é diretamente confiável para um servidor especificado.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Retorna o nome do controlador de domínio primário (PDC) para o domínio especificado.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Retorna o índice da primeira entrada de informações de exibição cujo nome começa com uma cadeia de caracteres especificada ou segue em ordem alfabética a cadeia de caracteres. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Retorna informações de conta de usuário, computador ou grupo global.                                                                             |



 

## <a name="group-functions"></a>Funções de grupo



| Função                                     | Descrição                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Cria um grupo global.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Adiciona um usuário a um grupo global existente.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Remove um grupo global, independentemente de o grupo ter ou não membros.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Remove um nome de usuário de um grupo global.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Lista todos os grupos globais em um servidor.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Retorna informações sobre um determinado grupo global.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Lista todos os membros de um determinado grupo global.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Define informações gerais sobre um grupo global.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Atribui membros a um novo grupo global; substitui os membros de um grupo existente. |



 

## <a name="local-group-functions"></a>Funções de grupo local



| Função                                                   | Descrição                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Cria um grupo local.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Adiciona um ou mais usuários ou grupos globais a um grupo local existente.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Exclui um grupo local, removendo todos os membros existentes do grupo.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Remove um ou mais membros de um grupo local existente.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Retorna informações sobre cada conta de grupo local em um servidor.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Retorna informações sobre uma conta de grupo local específica em um servidor. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Lista todos os membros de um grupo local especificado.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Define informações gerais sobre um grupo local.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Atribui membros a um grupo local.                                       |



 

## <a name="message-functions"></a>Funções de mensagem



| Função                                               | Descrição                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envia uma mensagem para um alias de mensagem registrado.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra um alias de mensagem na tabela de nome da mensagem.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Exclui um alias de mensagem da tabela de nome da mensagem.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Lista todos os aliases de mensagens armazenados na tabela nome da mensagem.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Retorna informações sobre um alias de mensagem específico na tabela de nomes de mensagem. |



 

## <a name="netfile-functions"></a>Funções de netfile



| Função                                | Descrição                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Força o fechamento de um recurso.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Retorna informações sobre arquivos abertos em um servidor.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Retorna informações sobre uma abertura específica de um recurso de servidor. |



 

## <a name="remote-utility-functions"></a>Funções do utilitário remoto



| Função                                                       | Descrição                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**NetRemoteComputerSupports**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | Consulta o redirecionador para recuperar os recursos opcionais aos quais um sistema remoto dá suporte. |
| [**NetRemoteTOD**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | Permite que os aplicativos acessem as informações de hora do dia em um servidor remoto.          |



 

## <a name="schedule-functions"></a>Funções de agendamento



| Função                                                                     | Descrição                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Envia um trabalho para ser executado em uma data e hora futuras especificadas.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Cancela um intervalo de trabalhos na fila para execução em um computador.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Lista os trabalhos em fila em um computador especificado.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Retorna informações sobre um trabalho específico na fila em um computador. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Recupera o nome da conta de serviço AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Define o nome e a senha da conta de serviço AT.                   |



 

## <a name="server-functions"></a>Funções de servidor



| Função                                       | Descrição                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Retorna uma lista de unidades de disco locais em um servidor.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Lista todos os servidores visíveis de um tipo específico (ou tipos) no domínio especificado. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Retorna informações de configuração sobre um servidor especificado.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Define os parâmetros operacionais de um servidor.                                        |



 

## <a name="server-and-workstation-transport-functions"></a>Funções de transporte de servidor e estação de trabalho



| Função                                                     | Descrição                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Associa um nome de servidor emulado a cada um dos protocolos de transporte nos quais um servidor está ativo. (Combina a funcionalidade da função [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) e da função [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) .)                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Desconecta cada protocolo de transporte de rede de um nome de servidor emulado definido por uma chamada anterior para a função **NetServerComputerNameAdd** .                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Associa o servidor especificado ao protocolo de transporte. (Essa função dá suporte apenas ao nível de informação [**\_ \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) de informações de transporte do servidor.)                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Associa o servidor especificado ao protocolo de transporte. (Essa função estendida dá suporte às informações de [**transporte do servidor \_ \_ info \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**Server \_ Transport \_ info \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)e [**Server \_ Transport \_ info \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) .) |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Desconecta o protocolo de transporte do servidor.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Enumera os protocolos de transporte gerenciados pelo servidor.                                                                                                                                                                                                                                                                   |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | Lista os protocolos de transporte que são gerenciados pelo redirecionador.                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>Usar funções



| Função                               | Descrição                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Cria uma conexão entre um computador local e um servidor.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Finaliza uma conexão com um recurso compartilhado.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Lista todas as conexões atuais entre o computador local e os recursos em servidores remotos. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Retorna informações sobre uma conexão a um recurso compartilhado.                              |



 

## <a name="user-functions"></a>Funções de usuário



| Função                                               | Descrição                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Adiciona uma conta de usuário e atribui um nível de senha e de privilégio.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Altera a senha de um usuário para um domínio ou servidor de rede especificado. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Exclui uma conta de usuário do servidor.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Lista todas as contas de usuário em um servidor.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Retorna uma lista de nomes de grupos globais aos quais um usuário pertence.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Retorna informações sobre uma conta de usuário específica em um servidor.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Retorna uma lista de nomes de grupos locais aos quais um usuário pertence.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Define associações de grupo global para uma conta de usuário especificada.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Define a senha e outros elementos de uma conta de usuário.             |



 

## <a name="user-modals-functions"></a>Funções de modal do usuário



| Função                                     | Descrição                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Retorna informações globais para todos os usuários e grupos globais no banco de dados de segurança, que é o banco de dados SAM (Gerenciador de contas de segurança) ou, no caso de controladores de domínio, o Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Define informações globais para todos os usuários e grupos globais no banco de dados de segurança.                                                                                                                       |



 

## <a name="validation-functions"></a>Funções de validação



| Função                                                               | Descrição                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera a memória que a função [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) aloca para o parâmetro *OutputArg* ,                                                                                      |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Permite que um aplicativo Verifique a conformidade de senha em relação a um banco de dados de conta fornecido pelo aplicativo e verifique se as senhas atendem aos requisitos de complexidade, duração, comprimento mínimo e reutilização de histórico de uma política de senha. |



 

## <a name="workstation-and-workstation-user-functions"></a>Funções de usuário da estação de trabalho e estação de trabalho



| Função                                           | Descrição                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | Retorna informações sobre os elementos de configuração para uma estação de trabalho.             |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | Configura uma estação de trabalho.                                                           |
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Lista informações sobre todos os usuários conectados no momento à estação de trabalho.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Retorna informações sobre um usuário conectado no momento.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Define as informações específicas do usuário para os elementos de configuração de uma estação de trabalho. |



 

## <a name="obsolete-functions"></a>Funções obsoletas

-   [**NetAccessAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**NetAccessCheck**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**NetAccessDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**NetAccessEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**NetAccessGetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**NetAccessGetUserPerms**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**NetAccessSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**NetAuditClear**](netauditclear.md)
-   [**NetAuditRead**](netauditread.md)
-   [**NetAuditWrite**](netauditwrite.md)
-   [**NetConfigGet**](netconfigget.md)
-   [**NetConfigGetAll**](netconfiggetall.md)
-   [**Netconfigset**](netconfigset.md)
-   [**NetErrorLogClear**](neterrorlogclear.md)
-   [**NetErrorLogRead**](neterrorlogread.md)
-   [**NetErrorLogWrite**](neterrorlogwrite.md)
-   [**NetLocalGroupAddMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**NetLocalGroupDelMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**NetServiceControl**](netservicecontrol.md)
-   [**NetServiceEnum**](netserviceenum.md)
-   [**NetServiceGetInfo**](netservicegetinfo.md)
-   [**NetServiceInstall**](netserviceinstall.md)
-   [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de rede do Windows](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 