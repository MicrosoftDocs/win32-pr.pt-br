---
description: O WMI usa um descritor de segurança padrão do Windows para controlar o acesso aos namespaces do WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Acesso a namespaces WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922602"
---
# <a name="access-to-wmi-namespaces"></a>Acesso a namespaces WMI

O WMI usa um *descritor de segurança* padrão do Windows para controlar o acesso aos namespaces do WMI. Quando você se conecta ao WMI, por meio do moniker "winmgmts" do WMI ou de uma chamada para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) ou [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), você se conecta a um namespace específico.

As informações a seguir são discutidas neste tópico:

-   [Segurança do namespace WMI](#wmi-namespace-security)
-   [Auditoria de namespace do WMI](#wmi-namespace-auditing)
-   [Tipos de eventos de namespace](#types-of-namespace-events)
-   [Configurações de acesso de namespace](#namespace-access-settings)
-   [Permissões padrão em namespaces do WMI](#default-permissions-on-wmi-namespaces)
-   [Tópicos relacionados](#related-topics)

## <a name="wmi-namespace-security"></a>Segurança do namespace WMI

O WMI mantém a segurança do namespace comparando o [*token de acesso*](/windows/desktop/SecGloss/a-gly) do usuário que se conecta ao namespace com o [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) do namespace. Para obter mais informações sobre a segurança do Windows, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).

Lembre-se de que, a partir do Windows Vista, o [UAC (controle de conta de usuário)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) afeta o acesso aos dados do WMI e o que pode ser configurado com o [*controle WMI*](gloss-w.md). Para obter mais informações, consulte [permissões padrão em namespaces do WMI](#default-permissions-on-wmi-namespaces) e [controle de conta de usuário e WMI](user-account-control-and-wmi.md).

O acesso aos namespaces do WMI também é afetado quando a conexão é de um computador remoto. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md), [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md)e [conectando por meio do firewall do Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Os provedores devem contar com a configuração de representação para a conexão para determinar se o script do cliente ou o aplicativo deve receber dados. Para obter mais informações sobre scripts e aplicativos cliente, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md). Para obter mais informações sobre a representação do [*provedor*](gloss-p.md) , consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

## <a name="wmi-namespace-auditing"></a>Auditoria de namespace do WMI

O WMI usa a [*SACL (listas de controle de acesso) do sistema*](/windows/desktop/SecGloss/s-gly) de namespace para auditar a atividade de namespace. Para habilitar a auditoria de namespaces do WMI, use a guia **segurança** no [*controle WMI*](gloss-w.md) para alterar as configurações de auditoria para o namespace.

A auditoria não é habilitada durante a instalação do sistema operacional. Para habilitar a auditoria, clique na guia **auditoria** na janela **segurança** padrão. Em seguida, você pode adicionar uma entrada de auditoria.

Política de Grupo para o computador local deve ser definido para permitir a auditoria. Você pode habilitar a auditoria executando o snap-in do MMC gpedit. msc e definindo o **acesso a objetos de auditoria** em configuração do **computador** configurações do Windows configurações de  >    >  **segurança**  >  **políticas locais**  >  **política de auditoria**.

Uma entrada de auditoria edita a SACL do namespace. Quando você adiciona uma entrada de auditoria, ela é um usuário, grupo, computador ou entidade de segurança interna. Depois de adicionar a entrada, você pode definir as operações de acesso que resultam em eventos de log de segurança. Por exemplo, para os usuários autenticados do grupo, você pode clicar em executar métodos. Essa configuração resulta em eventos de log de segurança sempre que um membro do grupo usuários autenticados executa um método nesse namespace. A ID do evento para eventos WMI é 4662.

Sua conta deve estar no grupo Administradores e em execução com privilégios elevados para alterar as configurações de auditoria. A conta interna de administrador também pode alterar a segurança ou a auditoria de um namespace. Para obter mais informações sobre como executar no modo elevado, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).

A auditoria WMI gera eventos de êxito ou falha para tentativas de acessar namespaces do WMI. O serviço não audita o êxito ou a falha das operações do provedor. Por exemplo, quando um script se conecta ao WMI e a um namespace, ele pode falhar porque a conta sob a qual o script está sendo executado não tem acesso a esse namespace ou pode tentar uma operação, como editar a DACL, que não é concedida.

Se você estiver executando sob uma conta no grupo Administradores, poderá exibir os eventos de auditoria de namespace na interface do usuário do **Visualizador de eventos** .

## <a name="types-of-namespace-events"></a>Tipos de eventos de namespace

O WMI rastreia os seguintes tipos de eventos no log de eventos de segurança:

-   Êxito na auditoria

    A operação deve concluir com êxito duas etapas para um êxito de auditoria. Primeiro, o WMI concede acesso ao aplicativo cliente ou script com base no SID do cliente e na DACL do namespace. Em segundo lugar, a operação solicitada corresponde aos direitos de acesso na SACL de namespace para esse usuário ou grupo.

-   Falha de auditoria

    O WMI nega o acesso ao namespace, mas a operação solicitada corresponde aos direitos de acesso na SACL de namespace para esse usuário ou grupo.

## <a name="namespace-access-settings"></a>Configurações de acesso de namespace

Você pode exibir os direitos de acesso do namespace para várias contas no controle WMI. Essas constantes são descritas em [**constantes direitos de acesso de namespace**](namespace-access-rights-constants.md). Você pode alterar o acesso a um namespace do WMI usando o controle WMI ou programaticamente. Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

As auditorias do WMI são alteradas em todas as permissões de acesso listadas na lista a seguir, exceto para a permissão habilitar remotamente. As alterações são registradas como êxito de auditoria ou falha correspondentes à permissão Editar segurança.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Métodos de execução
</dt> <dd>

Permite que o usuário execute métodos definidos em classes WMI. Corresponde à constante de permissão de acesso de **\_ \_ execução do método WBEM** .

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Gravação completa
</dt> <dd>

Permite o acesso completo de leitura, gravação e exclusão a classes WMI e instâncias de classe, tanto estática quanto dinâmica. Corresponde à constante de permissão de acesso do **\_ \_ \_ representante de gravação completa do WBEM** .

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Gravação parcial
</dt> <dd>

Permite o acesso de gravação a instâncias de classe WMI estáticas. Corresponde à constante de permissão de acesso do **\_ \_ \_ representante de gravação parcial do WBEM** .

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Gravação do provedor
</dt> <dd>

Permite o acesso de gravação a instâncias de classe WMI dinâmicas. Corresponde à constante de permissão de acesso do **\_ \_ provedor de gravação WBEM** .

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Habilitar conta
</dt> <dd>

Permite acesso de leitura a instâncias de classe WMI. Corresponde à constante de permissão **\_ habilitar** acesso do WBEM.

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Habilitação remota
</dt> <dd>

Permite o acesso ao namespace por computadores remotos. Corresponde à constante de permissão de acesso de acesso **\_ \_ remoto WBEM** .

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Ler segurança
</dt> <dd>

Permite o acesso somente leitura às configurações de DACL. Corresponde à constante de permissão de acesso do **\_ controle de leitura** .

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Editar segurança
</dt> <dd>

Permite o acesso de gravação às configurações de DACL. Corresponde à constante de permissão gravar acesso de **\_ DAC** .

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Permissões padrão em namespaces do WMI

Os grupos de segurança padrão são:

-   Usuários Autenticados
-   LOCAL SERVICE
-   SERVIÇO DE REDE
-   Administradores (no computador local)

As permissões de acesso padrão para os usuários autenticados, o serviço LOCAL e o serviço de rede são:

-   Executar métodos
-   Gravação completa
-   Habilitar conta

As contas no grupo Administradores têm todos os direitos disponíveis, incluindo a edição de descritores de segurança. No entanto, devido ao UAC (controle de conta de usuário), o controle WMI ou o script deve estar sendo executado com segurança elevada. Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).

Às vezes, um script ou aplicativo deve habilitar um privilégio de administrador, como **SeSecurityPrivilege**, para realizar uma operação. Por exemplo, um script pode executar o método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) da classe [**de \_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) sem **SeSecurityPrivilege** e obter as informações de segurança na [*DACL (lista de controle de acesso discricionário)*](/windows/desktop/SecGloss/d-gly) do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)do objeto da impressora. No entanto, as informações de SACL não são retornadas para o script, a menos que o privilégio **SeSecurityPrivilege** esteja disponível e habilitado para a conta. Se a conta não tiver o privilégio disponível, ela não poderá ser habilitada. Para obter mais informações, consulte [executando operações privilegiadas](executing-privileged-operations.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> </dl>

 

 
