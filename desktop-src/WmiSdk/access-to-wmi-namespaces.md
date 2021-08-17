---
description: O WMI usa um descritor Windows segurança padrão para controlar o acesso a namespaces WMI.
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
ms.openlocfilehash: b750c8dee2b95597636620dc54ad193cb762cd259b2bf7149c52996e85e09b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926022"
---
# <a name="access-to-wmi-namespaces"></a>Acesso a namespaces WMI

O WMI usa um descritor Windows *segurança padrão* para controlar o acesso a namespaces WMI. Quando você se conecta ao WMI, seja por meio do moniker "winmgmts" do WMI ou de uma chamada para [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) ou [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), você se conecta a um namespace específico.

As seguintes informações são discutidas neste tópico:

-   [Segurança do namespace WMI](#wmi-namespace-security)
-   [Auditoria de namespace WMI](#wmi-namespace-auditing)
-   [Tipos de eventos de namespace](#types-of-namespace-events)
-   [Namespace Access Configurações](#namespace-access-settings)
-   [Permissões padrão em namespaces WMI](#default-permissions-on-wmi-namespaces)
-   [Tópicos relacionados](#related-topics)

## <a name="wmi-namespace-security"></a>Segurança do namespace WMI

O WMI mantém a segurança do namespace comparando o [*token*](/windows/desktop/SecGloss/a-gly) de acesso do usuário que se conecta ao namespace com o [*descritor de*](/windows/desktop/SecGloss/s-gly) segurança do namespace. Para obter mais informações sobre Windows segurança, consulte [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).

Esteja ciente de que, a partir do Windows Vista, o [UAC (Controle](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) de Conta de Usuário) afeta o acesso aos dados WMI e o que pode ser configurado com o [*controle WMI*](gloss-w.md). Para obter mais informações, [consulte Permissões padrão em namespaces WMI](#default-permissions-on-wmi-namespaces) e Controle de Conta de Usuário e [WMI](user-account-control-and-wmi.md).

O acesso a namespaces WMI também é afetado quando a conexão é de um computador remoto. Para obter mais informações, consulte Conectando-se ao [WMI](connecting-to-wmi-on-a-remote-computer.md)em um computador remoto, Proteger uma conexão [WMI](securing-a-remote-wmi-connection.md)remota e Conectando-se por meio [Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Os provedores devem depender da configuração de representação para que a conexão determine se o script do cliente ou o aplicativo deve receber dados. Para obter mais informações sobre scripts e aplicativos cliente, consulte [Configurando a segurança do processo de aplicativo cliente.](setting-client-application-process-security.md) Para obter mais informações sobre [*a representação*](gloss-p.md) do provedor, consulte [Desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

## <a name="wmi-namespace-auditing"></a>Auditoria de namespace WMI

O WMI usa o [*SACL (listas*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema) do namespace para auditar a atividade do namespace. Para habilitar a auditoria de namespaces WMI, use a guia Segurança no Controle [*WMI*](gloss-w.md) para alterar as configurações de auditoria do namespace. 

A auditoria não está habilitada durante a instalação do sistema operacional. Para habilitar a auditoria, clique **na guia Auditoria** na janela **Segurança** padrão. Em seguida, você pode adicionar uma entrada de auditoria.

Política de Grupo para o computador local deve ser definido para permitir a auditoria. Você pode habilitar a auditoria executando o snap-in do MMC Gpedit.msc e definindo **Audit Object Access** em Configuração do  >  **Computador Windows Configurações** Segurança  >  **Configurações**  >    >  Política de Auditoria de Políticas Locais .

Uma entrada de auditoria edita a SACL do namespace. Quando você adiciona uma entrada de auditoria, é um usuário, grupo, computador ou entidade de segurança interna. Depois de adicionar a entrada, você pode definir as operações de acesso que resultam em eventos de Log de Segurança. Por exemplo, para o grupo Usuários Autenticados, você pode clicar em Executar Métodos. Essa configuração resulta em eventos do Log de Segurança sempre que um membro do grupo Usuários Autenticados executa um método nesse namespace. A ID do evento para eventos WMI é 4662.

Sua conta deve estar no grupo Administradores e em execução com privilégios elevados para alterar as configurações de auditoria. A conta de Administrador interna também pode alterar a segurança ou a auditoria de um namespace. Para obter mais informações sobre como executar no modo elevado, consulte [Controle de Conta de Usuário e WMI](user-account-control-and-wmi.md).

A auditoria WMI gera eventos de êxito ou falha para tentativas de acessar namespaces WMI. O serviço não audita o êxito ou a falha das operações do provedor. Por exemplo, quando um script se conecta ao WMI e a um namespace, ele pode falhar porque a conta sob a qual o script está sendo executado não tem acesso a esse namespace ou pode tentar uma operação, como editar a DACL, que não é concedida.

Se você estiver executando em uma conta no grupo Administradores, poderá exibir os eventos de auditoria de namespace na interface **Visualizador de Eventos** usuário.

## <a name="types-of-namespace-events"></a>Tipos de eventos de namespace

O WMI acompanha os seguintes tipos de eventos no Log de Eventos de Segurança:

-   Auditoria bem-sucedida

    A operação deve concluir com êxito duas etapas para um Êxito de Auditoria. Primeiro, o WMI concede acesso ao aplicativo cliente ou script com base no SID do cliente e na DACL do namespace. Em segundo lugar, a operação solicitada corresponde aos direitos de acesso no SACL do namespace para esse usuário ou grupo.

-   Falha de auditoria

    O WMI nega acesso ao namespace, mas a operação solicitada corresponde aos direitos de acesso no SACL do namespace para esse usuário ou grupo.

## <a name="namespace-access-settings"></a>Namespace Access Configurações

Você pode exibir os direitos de acesso de namespace para várias contas no controle WMI. Essas constantes são descritas em [**Constantes de Direitos de Acesso do Namespace**](namespace-access-rights-constants.md). Você pode alterar o acesso a um namespace WMI usando o Controle WMI ou programaticamente. Para obter mais informações, consulte [Alterando a segurança de acesso em objetos securáveis.](changing-access-security-on-securable-objects.md)

O WMI audita as alterações em todas as permissões de acesso listadas na lista a seguir, exceto para a permissão Habilitar Remotamente. As alterações são registradas como êxito ou falha de auditoria correspondentes à permissão Editar Segurança.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Executar métodos
</dt> <dd>

Permite que o usuário execute métodos definidos em classes WMI. Corresponde à constante de permissão de acesso **\_ WBEM METHOD \_ EXECUTE.**

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Gravação completa
</dt> <dd>

Permite acesso completo de leitura, gravação e exclusão a classes WMI e instâncias de classe, tanto estáticas quanto dinâmicas. Corresponde à constante **de permissão de acesso do WBEM FULL WRITE \_ \_ \_ REP.**

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Gravação parcial
</dt> <dd>

Permite acesso de gravação a instâncias de classe WMI estáticas. Corresponde à constante de **permissão de acesso \_ WBEM PARTIAL WRITE \_ \_ REP.**

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Gravação do provedor
</dt> <dd>

Permite acesso de gravação a instâncias de classe WMI dinâmicas. Corresponde à constante **de permissão de acesso WBEM WRITE \_ \_ PROVIDER.**

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Habilitar Conta
</dt> <dd>

Permite acesso de leitura a instâncias de classe WMI. Corresponde à constante de permissão de acesso ENABLE do **WBEM. \_**

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Habilitar remotamente
</dt> <dd>

Permite o acesso ao namespace por computadores remotos. Corresponde à constante **de permissão de acesso REMOTO \_ \_ DO WBEM.**

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Ler Segurança
</dt> <dd>

Permite o acesso somente leitura às configurações de DACL. Corresponde à constante **de permissão de acesso READ \_ CONTROL.**

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Editar segurança
</dt> <dd>

Permite acesso de gravação às configurações de DACL. Corresponde à constante **de permissão de acesso WRITE \_ DAC.**

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Permissões padrão em namespaces WMI

Os grupos de segurança padrão são:

-   Usuários Autenticados
-   LOCAL SERVICE
-   SERVIÇO DE REDE
-   Administradores (no computador local)

As permissões de acesso padrão para usuários autenticados, SERVIÇO LOCAL e SERVIÇO DE REDE são:

-   Executar métodos
-   Gravação completa
-   Habilitar conta

As contas no grupo Administradores têm todos os direitos disponíveis para elas, incluindo a edição de descritores de segurança. No entanto, devido ao UAC (Controle de Conta de Usuário), o controle WMI ou o script devem estar em execução com segurança elevada. Para obter mais informações, consulte [Controle de conta de usuário e WMI](user-account-control-and-wmi.md).

Às vezes, um script ou aplicativo deve habilitar um privilégio de administrador, como **SeSecurityPrivilege**, para executar uma operação. Por exemplo, um script pode executar o método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) da classe [**Impressora \_ Win32**](/windows/desktop/CIMWin32Prov/win32-printer) sem **SeSecurityPrivilege** e obter as informações de segurança na [*DACL (lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) do descritor de segurança do objeto [*de*](/windows/desktop/SecGloss/s-gly)impressora . No entanto, as informações sacl não são retornadas para o script, a menos que o privilégio **SeSecurityPrivilege** esteja disponível e habilitado para a conta. Se a conta não tiver o privilégio disponível, ela não poderá ser habilitada. Para obter mais informações, consulte [Executando operações privilegiadas.](executing-privileged-operations.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> </dl>

 

 
