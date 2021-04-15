---
title: 'Instalação e configuração para Gerenciamento Remoto do Windows '
description: Para que os scripts do Gerenciamento Remoto do Windows (WinRM) sejam executados e para que a ferramenta de linha de comando do **WinRM** execute operações de dados, o gerenciamento remoto do Windows (WinRM) deve estar instalado e configurado.
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: 4ebe4094984f237a3c8949392e3e9a6b47b8afe6
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/04/2021
ms.locfileid: "104500121"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Instalação e configuração para Gerenciamento Remoto do Windows

Para que os scripts do Gerenciamento Remoto do Windows (WinRM) sejam executados e para que a ferramenta de linha de comando do **WinRM** execute operações de dados, o gerenciamento remoto do Windows (WinRM) deve estar instalado e configurado.

Esses elementos também dependem da configuração do WinRM.

- A ferramenta de linha de comando do [shell remoto do Windows](./windows-remote-management-glossary.md#w) (**WinRS**).
- [Encaminhamento de eventos](./windows-remote-management-glossary.md#e).
- Comunicação remota do Windows PowerShell 2,0.

## <a name="where-winrm-is-installed"></a>Onde o WinRM está instalado

O WinRM é instalado automaticamente com todas as versões do sistema operacional Windows com suporte no momento.

## <a name="configuration-of-winrm-and-ipmi"></a>Configuração do WinRM e do IPMI

Esses componentes do [provedor WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) do WinRM e do [IPMI (interface de gerenciamento de plataforma inteligente)](./windows-remote-management-glossary.md#i) são instalados com o sistema operacional.

- O serviço WinRM é iniciado automaticamente no Windows Server 2008 e em diante (no Windows Vista, você precisa iniciar o serviço manualmente).
- Por padrão, nenhum [ouvinte](./windows-remote-management-glossary.md#l) do WinRM está configurado. Mesmo que o serviço WinRM esteja em execução, WS-Management [mensagens](./windows-remote-management-glossary.md#m) de protocolo que solicitam dados não podem ser recebidas nem enviadas.
- O firewall de conexão com a Internet (ICF) bloqueia o acesso às portas.

Use o comando **WinRM** para localizar ouvintes e endereços digitando o comando a seguir em um prompt de comando.

```console
winrm e winrm/config/listener
```

Para verificar o estado dos parâmetros de configuração, digite o comando a seguir.

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>Configuração padrão rápida

Você pode habilitar o protocolo WS-Management no computador local e definir a configuração padrão para gerenciamento remoto com o comando `winrm quickconfig` .

O `winrm quickconfig` comando (ou a versão abreviada `winrm qc` ) executa essas operações.

- Inicia o serviço WinRM e define o tipo de inicialização do serviço como iniciar automaticamente.
- Configura um ouvinte para as portas que enviam e recebem WS-Management [mensagens](./windows-remote-management-glossary.md#m) de protocolo usando http ou HTTPS em qualquer endereço IP.
- Define as exceções do ICF para o serviço WinRM e abre as portas para HTTP e HTTPS.

> [!NOTE]
> O `winrm quickconfig` comando cria uma exceção de firewall somente para o perfil de usuário atual. Se o perfil de firewall for alterado por qualquer motivo, você deverá executar `winrm quickconfig` o para habilitar a exceção de firewall para o novo perfil; caso contrário, a exceção poderá não estar habilitada.

Para recuperar informações sobre como personalizar uma configuração, digite `winrm help config` em um prompt de comando.

### <a name="to-configure-winrm-with-default-settings"></a>Para configurar o WinRM com as configurações padrão

1. Digite `winrm quickconfig` em um prompt de comando.

   Se você não estiver executando sob a conta de administrador do computador local, deverá selecionar **Executar como administrador** no menu **Iniciar** ou usar o comando **runas** em um prompt de comando.

2. Quando a ferramenta exibe **fazer essas alterações \[ y/n \] ?**, digite **y**.

   Se a configuração for bem-sucedida, a saída a seguir será exibida.

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. Mantenha as configurações padrão dos componentes cliente e servidor do WinRM ou personalize-os. Por exemplo, talvez seja necessário adicionar determinados computadores remotos à lista TrustedHosts de configuração do cliente.

   Você deve configurar uma lista de hosts confiáveis quando a autenticação mútua não puder ser estabelecida. O Kerberos permite a autenticação mútua, mas não pode ser usado somente em domínios de grupos de &mdash; domínio. Uma prática recomendada ao configurar hosts confiáveis para um grupo de trabalho é tornar a lista o mais restrito possível.

4. Crie um ouvinte HTTPS digitando o comando `winrm quickconfig -transport:https` . Lembre-se de que você deve abrir a porta 5986 para que o transporte HTTPS funcione.

## <a name="listener-and-ws-management-protocol-default-settings"></a>Configurações padrão do protocolo ouvinte e WS-Management

Para obter a configuração do ouvinte, digite `winrm enumerate winrm/config/listener` em um prompt de comando. Os ouvintes são definidos por um transporte (HTTP ou HTTPS) e um endereço IPv4 ou IPv6.

`winrm quickconfig` cria as seguintes configurações padrão para um ouvinte. Você pode criar mais de um ouvinte. Para obter mais informações, digite `winrm help config` em um prompt de comando.

### <a name="address"></a>Endereço

Especifica o endereço para o qual este ouvinte foi criado.

### <a name="transport"></a>Transport

Especifica o transporte a ser usado para enviar e receber respostas e solicitações do protocolo WS-Management. O valor deve ser *http* ou *https*. O padrão é *http*.

### <a name="port"></a>Porta

Especifica a porta TCP para a qual este ouvinte é criado.

**WinRM 2,0:** A porta HTTP padrão é 5985.

### <a name="hostname"></a>Nome do host

Especifica o nome do host do computador no qual o serviço WinRM está em execução. O valor deve ser um nome de domínio totalmente qualificado ou uma cadeia de caracteres literal IPv4 ou IPv6, ou um caractere curinga.

### <a name="enabled"></a>habilitado

Especifica se o ouvinte está habilitado ou desabilitado. O valor padrão é *True*.

### <a name="urlprefix"></a>URLPrefix

Especifica um prefixo de URL no qual aceitar solicitações HTTP ou HTTPS. Esta é uma cadeia de caracteres que contém apenas os caracteres de a-z, A-Z, 9-0, sublinhado ( \_ ) e barra (/). A cadeia de caracteres não deve começar com ou terminar com uma barra (/). Por exemplo, se o nome do computador for SampleMachine, o cliente WinRM especificará https://SampleMachine/< *URLPrefix*> no endereço de destino. O prefixo de URL padrão é "WSMan".

### <a name="certificatethumbprint"></a>CertificateThumbprint

Especifica a impressão digital do certificado de serviço. Esse valor representa uma cadeia de caracteres de valores hexadecimais de dois dígitos encontrada no campo impressão digital do certificado. Essa cadeia de caracteres contém o hash SHA-1 do certificado. Os certificados são utilizados na autenticação baseada em certificado do cliente. Os certificados podem ser mapeados somente para contas de usuário locais e não funcionam com contas de domínio.

### <a name="listeningon"></a>ListeningOn

Especifica os endereços IPv4 e IPv6 que o ouvinte usa. Por exemplo: "111.0.0.1, 111.222.333.444,:: 1, 1000:2000:2C: 3: c19:9ec8: a715:5e24, 3FFE: 8311: ffff: f70f: 0:5efe: 111.222.333.444, FE80:: 5efe: 111.222.333.444% 8, FE80:: c19:9ec8: a715:5e24% 6".

## <a name="protocol-default-settings"></a>Configurações padrão de protocolo

Muitas das definições de configuração, como MaxEnvelopeSizekb ou SoapTraceEnabled, determinam como os componentes do cliente e do servidor WinRM interagem com o protocolo WS-Management. A lista a seguir descreve as definições de configuração disponíveis.

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

Especifica os dados do protocolo SOAP (Simple Object Access Protocol) em kilobytes. O padrão é 150 quilobytes.

> [!NOTE]  
> O comportamento não será suportado se MaxEnvelopeSizekb for definido como um valor maior que 1039440.

### <a name="maxtimeoutms"></a>MaxTimeoutms

Especifica o tempo limite máximo, em milissegundos, que pode ser usado para qualquer solicitação que não sejam solicitações de pull. O padrão é 60000.

### <a name="maxbatchitems"></a>MaxBatchItems

Especifica o número máximo de elementos que podem ser usados em uma resposta de recepção. O padrão é 32000.

### <a name="maxproviderrequests"></a>MaxProviderRequests

Especifica o número máximo de solicitações simultâneas permitido pelo serviço. O padrão é 25.

**WinRM 2,0:** Essa configuração é preterida e é definida como somente leitura.

## <a name="winrm-client-default-configuration-settings"></a>Definições de configuração padrão do cliente WinRM

A versão do cliente do WinRM tem as seguintes definições de configuração padrão.

### <a name="networkdelayms"></a>NetworkDelayms

Especifica o tempo extra, em milissegundos, que o computador cliente aguarda para acomodar o tempo de atraso de rede. O padrão é 5000 milissegundos.

### <a name="urlprefix"></a>URLPrefix

Especifica um prefixo de URL no qual aceitar solicitações HTTP ou HTTPS. O prefixo de URL padrão é "WSMan".

### <a name="allowunencrypted"></a>AllowUnencrypted

Permite que o computador cliente solicite tráfego não criptografado. Por padrão, o computador cliente requer o tráfego de rede criptografado e essa configuração é *falsa*.

### <a name="basic"></a>Básico

Permite que o computador cliente use a autenticação básica. A autenticação básica é um esquema no qual o nome de usuário e a senha são enviados em texto não criptografado para o servidor ou proxy. Esse método é o método menos seguro de autenticação. O padrão é *True*.

### <a name="digest"></a>Digest

Permite que o cliente use a autenticação Digest. É um esquema de desafio/resposta de autenticação que utiliza uma cadeia de caracteres de dados do servidor especificado para o desafio. Apenas o computador cliente pode iniciar uma solicitação de autenticação Digest. O computador cliente envia uma solicitação ao servidor para autenticar e recebe uma cadeia de caracteres do token do servidor. Em seguida, o computador cliente envia a solicitação de recurso, incluindo o nome de usuário e um hash criptográfico da senha combinada com a cadeia de caracteres do token. A autenticação Digest tem suporte para HTTP e HTTPS. Os aplicativos e scripts de cliente do shell do WinRM podem especificar a autenticação Digest, mas o serviço WinRM não aceita a autenticação Digest. O padrão é *True*.

> [!NOTE]
> A autenticação Digest por HTTP não é considerada segura.

### <a name="certificate"></a>Certificado

Permite que o cliente use a autenticação baseada em certificado do cliente. A autenticação baseada em certificado é um esquema no qual o servidor autentica um cliente identificado por um certificado X509. O padrão é *True*.

### <a name="kerberos"></a>Kerberos

Permite que o cliente use a autenticação Kerberos. A autenticação Kerberos é um esquema no qual o cliente e o servidor autenticam mutuamente usando certificados Kerberos. O padrão é *True*.

### <a name="negotiate"></a>Negotiate

Permite que o cliente use a autenticação Negotiate. Negociar a autenticação é um esquema no qual o cliente envia uma solicitação ao servidor para autenticar. O servidor determina se deve usar o protocolo Kerberos ou NTLM. O protocolo Kerberos é selecionado para autenticar uma conta de domínio e NTLM é selecionado para contas de computador local. O nome de usuário deve ser especificado no \\ \_ formato de nome de usuário de domínio para um usuário de domínio. O nome de usuário deve ser especificado no \_ formato " \\ nome de usuário do nome do servidor \_ " para um usuário local em um computador servidor. O padrão é *True*.

### <a name="credssp"></a>CredSSP

Permite que o cliente use a autenticação do Credential Security Support Provider (CredSSP). O CredSSP permite que um aplicativo delegue as credenciais do usuário do computador cliente para o servidor de destino. O padrão é *False*.

### <a name="defaultports"></a>DefaultPorts

Especifica as portas que o cliente usará para HTTP ou HTTPS.

**WinRM 2,0:** A porta HTTP padrão é 5985 e a porta HTTPS padrão é 5986.

### <a name="trustedhosts"></a>TrustedHosts

Especifica a lista de computadores remotos que são confiáveis. Outros computadores em um grupo de trabalho ou computadores em um domínio diferente devem ser adicionados a essa lista.

> [!Note]
> Os computadores na lista TrustedHosts não são autenticados. O cliente pode enviar informações de credenciais para esses computadores.

Se um endereço IPv6 for especificado para um TrustedHost, o endereço deverá ser colocado entre colchetes, conforme demonstrado pelo seguinte comando do utilitário WinRM: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .

Para obter mais informações sobre como adicionar computadores à lista TrustedHosts, digite `winrm help config` .

## <a name="winrm-service-default-configuration-settings"></a>Definições de configuração padrão do serviço WinRM

A versão do serviço do WinRM tem as seguintes definições de configuração padrão.

### <a name="rootsddl"></a>RootSDDL

Especifica o descritor de segurança que controla o acesso remoto ao ouvinte. O padrão é "O:NSG: BAD: P (A;; GA;;; BA) (A;; GR;;; ER) S:P (AU; FA; GA;;; WD) (AU; SA; GWGX;;; WD) ".

### <a name="maxconcurrentoperations"></a>MaxConcurrentOperations

O número máximo de operações simultâneas. O padrão é 100.

**WinRM 2,0:** A configuração MaxConcurrentOperations é preterida e está definida como somente leitura. Essa configuração foi substituída por MaxConcurrentOperationsPerUser.

### <a name="maxconcurrentoperationsperuser"></a>MaxConcurrentOperationsPerUser

Especifica o número máximo de operações simultâneas que qualquer usuário pode abrir remotamente no mesmo sistema. O padrão é 1500.

### <a name="enumerationtimeoutms"></a>EnumerationTimeoutms

Especifica o tempo limite de ociosidade em milissegundos entre as mensagens de pull. O padrão é 60000.

### <a name="maxconnections"></a>MaxConnections

Especifica o número máximo de solicitações ativas que o serviço pode processar simultaneamente. O padrão é 300.

**WinRM 2,0:** O padrão é 25.

### <a name="maxpacketretrievaltimeseconds"></a>MaxPacketRetrievalTimeSeconds

Especifica o período máximo de tempo, em segundos, que o serviço WinRM leva para recuperar um pacote. O padrão é 120 segundos.

### <a name="allowunencrypted"></a>AllowUnencrypted

Permite que o computador cliente solicite tráfego não criptografado. O padrão é *False*.

### <a name="basic"></a>Básico

Permite que o serviço WinRM use a autenticação básica. O padrão é *False*.

### <a name="certificate"></a>Certificado

Permite que o serviço WinRM use a autenticação baseada em certificado do cliente. O padrão é *False*.

### <a name="kerberos"></a>Kerberos

Permite que o serviço WinRM use a autenticação Kerberos. O padrão é *True*.

### <a name="negotiate"></a>Negotiate

Permite que o serviço WinRM use a autenticação de negociação. O padrão é *True*.

### <a name="credssp"></a>CredSSP

Permite que o serviço WinRM use a autenticação do Credential Security Support Provider (CredSSP). O padrão é *False*.

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

Define a política para requisitos de token de associação de canal em solicitações de autenticação. O padrão é *relaxado*.

### <a name="defaultports"></a>DefaultPorts

Especifica as portas que o serviço WinRM usará para HTTP ou HTTPS.

**WinRM 2,0:** A porta HTTP padrão é 5985 e a porta HTTPS padrão é 5986.

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter e IPv6Filter

Especifica os endereços IPv4 ou IPv6 que os ouvintes podem usar. Os padrões são IPv4Filter = \* e IPv6Filter = \* .

**IPv4:** Uma cadeia de caracteres literal IPv4 consiste em quatro números decimais pontilhados, cada um no intervalo de 0 a 255. Por exemplo: 192.168.0.0.

**IPv6:** Uma cadeia de caracteres literal do IPv6 é colocada entre colchetes e contém números hexadecimais separados por dois-pontos. Por exemplo:: \[ : 1 \] ou \[ 3ffe: ffff:: 6ECB: 0101 \] .

### <a name="enablecompatibilityhttplistener"></a>EnableCompatibilityHttpListener

Especifica se o ouvinte de HTTP de compatibilidade está habilitado. Se essa configuração for *verdadeira*, o ouvinte escutará na porta 80 além da porta 5985. O padrão é *False*.

### <a name="enablecompatibilityhttpslistener"></a>EnableCompatibilityHttpsListener

Especifica se o ouvinte de HTTPS de compatibilidade está habilitado. Se essa configuração for *verdadeira*, o ouvinte escutará na porta 443 além da porta 5986. O padrão é *False*.

## <a name="winrs-default-configuration-settings"></a>Definições de configuração padrão do WinRS

`winrm quickconfig` também define as configurações padrão do **WinRS** .

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

Permite o acesso a shells remotos. Se você definir esse parâmetro como *false*, as novas conexões de shell remoto serão rejeitadas pelo servidor. O padrão é *True*.

### <a name="idletimeout"></a>IdleTimeout

Especifica o tempo máximo, em milissegundos, que o shell remoto permanecerá aberto quando não houver nenhuma atividade de usuário no shell remoto. O shell remoto é excluído automaticamente após o tempo especificado.

**WinRM 2,0:** O padrão é 180000. O valor mínimo é 60000. Definir esse valor inferior a 60000 não terá efeito sobre o tempo limite.

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

Especifica o número máximo de usuários que podem executar simultaneamente operações remotas no mesmo computador por meio de um shell remoto. Novas conexões de shell remoto serão rejeitadas se excederem o limite especificado. O padrão é 5.

### <a name="maxshellruntime"></a>MaxShellRunTime

Especifica o tempo máximo, em milissegundos, que o comando remoto ou o script pode executar. O padrão é 28,8 milhões.

**WinRM 2,0:** A configuração MaxShellRunTime é definida como somente leitura. Alterar o valor de MaxShellRunTime não terá nenhum efeito sobre os shells remotos.

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

Especifica o número máximo de processos que qualquer operação de shell tem permissão para iniciar. Um valor 0 permite um número ilimitado de processos. O padrão é 15.

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

Especifica a quantidade máxima de memória alocada por shell, incluindo os processos filho do Shell. O padrão é 150 MB.

### <a name="maxshellsperuser"></a>MaxShellsPerUser

Especifica o número máximo de shells simultâneos que um usuário pode abrir remotamente no mesmo computador. Se essa configuração de política estiver habilitada, o usuário não poderá abrir novos shells remotos se a contagem exceder o limite especificado. Se esta configuração de política estiver desabilitada ou não estiver configurada, o limite será definido para 5 shells remotos por usuário por padrão.

## <a name="configuring-winrm-with-group-policy"></a>Configurando o WinRM com o Política de Grupo

Use o editor de Política de Grupo para configurar o shell remoto do Windows e o WinRM para computadores em sua empresa.

### <a name="to-configure-with-group-policy"></a>Para configurar com Política de Grupo

1. Abra uma janela de Prompt de comando como administrador.
2. No prompt de comando, digite `gpedit.msc` . A janela **Editor de objeto de política de grupo** é aberta.
3. Localize o **gerenciamento remoto do Windows** e o **Windows Remote Shell** política de grupo Objects (GPO) em **configuração do computador \\ modelos administrativos componentes do \\ Windows**.
4. Na guia **estendida** , selecione uma configuração para ver uma descrição. Clique duas vezes em uma configuração para editá-la.

## <a name="windows-firewall-and-winrm-20-ports"></a>Portas do firewall do Windows e do WinRM 2,0

A partir do WinRM 2,0, as portas de ouvinte padrão configuradas pelo `Winrm quickconfig` são a porta 5985 para transporte http e a porta 5986 para https. Os ouvintes do WinRM podem ser configurados em qualquer porta arbitrária.

Se um computador for atualizado para o WinRM 2,0, os ouvintes configurados anteriormente serão migrados e ainda receberão o tráfego.

## <a name="winrm-installation-and-configuration-notes"></a>Notas de instalação e configuração do WinRM

O WinRM não depende de nenhum outro serviço, exceto WinHttp. Se o serviço de administração do IIS estiver instalado no mesmo computador, você poderá ver mensagens que indicam que o WinRM não pode ser carregado antes de Serviços de Informações da Internet (IIS). No entanto, o WinRM não depende realmente do IIS &mdash; que essas mensagens ocorrem porque a ordem de carregamento garante que o serviço IIS seja iniciado antes do serviço http. O WinRM requer que `WinHTTP.dll` seja registrado.

Se o cliente de firewall do ISA2004 estiver instalado no computador, ele poderá fazer com que um cliente do Web Services para gerenciamento (WS-Management) pare de responder. Para evitar esse problema, instale o ISA2004 firewall SP1.

Se dois serviços de escuta com endereços IP diferentes estiverem configurados com o mesmo número de porta e nome do computador, o WinRM escutará ou receberá mensagens em apenas um endereço. Isso ocorre porque os prefixos de URL usados pelo protocolo WS-Management são os mesmos.

## <a name="ipmi-driver-and-provider-installation-notes"></a>Notas de instalação do driver e do provedor IPMI

O driver pode não detectar a existência de drivers IPMI que não são da Microsoft. Se o driver não for iniciado, talvez seja necessário desabilitá-lo.

Se os recursos do [BMC (Baseboard Management Controller)](./windows-remote-management-glossary.md#b) aparecerem no BIOS do sistema, a ACPI (plug and Play) detectará o hardware do BMC e instalará automaticamente o driver IPMI. Plug and Play suporte pode não estar presente em todos os BMCs. Se o BMC for detectado pelo Plug and Play, um dispositivo desconhecido aparecerá em Gerenciador de Dispositivos antes de o componente de gerenciamento de hardware ser instalado. Quando o driver é instalado, um novo componente, o dispositivo compatível com IPMI genérico do Microsoft ACPI, aparece em Gerenciador de Dispositivos.

Se o seu sistema não detectar automaticamente o BMC e instalar o driver, mas um BMC foi detectado durante o processo de instalação, você deverá criar o dispositivo BMC. Para fazer isso, digite o seguinte comando no prompt de comando: `Rundll32 ipmisetp.dll, AddTheDevice` . Depois que esse comando é executado, o dispositivo IPMI é criado e aparece em Gerenciador de Dispositivos. Se você desinstalar o componente de gerenciamento de hardware, o dispositivo será removido.

Para obter mais informações, consulte [introdução ao gerenciamento de hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

O provedor de IPMI coloca as classes de hardware no [namespace](/windows/desktop/WmiSdk/gloss-n) de **\\ hardware raiz** do WMI. Para obter mais informações sobre as classes de hardware, consulte [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). Para obter mais informações sobre *namespaces* WMI, consulte [arquitetura WMI](/windows/desktop/WmiSdk/wmi-architecture).

## <a name="wmi-plug-in-configuration-notes"></a>Observações de configuração de plug-in WMI

A partir do Windows 8 e do Windows Server 2012, os [plug-ins WMI](./windows-remote-management-glossary.md#w) têm suas próprias configurações de segurança. Para que um usuário normal ou de energia (não administrador) possa usar o *plug-in WMI*, você precisa habilitar o acesso para esse usuário após a configuração do [ouvinte](./windows-remote-management-glossary.md#l) . Primeiro, você deve configurar o usuário para acesso remoto ao [WMI](./windows-remote-management-glossary.md#w) por meio de uma destas etapas.

- Execute `lusrmgr.msc` para adicionar o usuário ao grupo **WinRMRemoteWMIUsers \_ \_** na janela **usuários e grupos locais** ou
- Use a ferramenta de linha de comando **WinRM** para configurar o descritor de segurança para o [*namespace*](./windows-remote-management-glossary.md#n) do [plug-in do WMI](./windows-remote-management-glossary.md#w), da seguinte maneira: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .

Quando a interface do usuário for exibida, adicione o usuário.

Depois de configurar o usuário para acesso remoto ao [WMI](./windows-remote-management-glossary.md#w), você deve configurar o *WMI* para permitir que o usuário acesse o plug-in. Para fazer isso, execute `wmimgmt.msc` para modificar a segurança do *WMI* para o [namespace](./windows-remote-management-glossary.md#n) a ser acessado na janela **controle WMI** .

A maioria das classes WMI para gerenciamento está no namespace **raiz \\ cimv2** .