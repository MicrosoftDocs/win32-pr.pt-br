---
description: Windows O instalador é a solução recomendada para a instalação e instalação de aplicativos no Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: guia baseado em função para Windows Installer documentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f886050f3bb0256f6f0f993e613be940cee9cd2fe748b2d17b5dc0f0f84a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625858"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>guia baseado em função para Windows Installer documentação

Windows O instalador é a solução recomendada para a instalação e instalação de aplicativos no Windows. Portanto, algumas das informações contidas neste SDK serão de interesse de uma ampla gama de desenvolvimento de software e profissionais de ti. Esta seção é fornecida como um guia para os leitores que preferem ver links para tópicos organizados por funções profissionais e cenários comuns de tarefas. Como as funções podem diferir muito entre as organizações, o agrupamento a seguir só deve ser considerado um guia para um local para começar a pesquisar as informações necessárias.

-   [Desenvolvedores de aplicativos](#application-developers)
-   [Autores de instalação](#setup-authors)
-   [Profissionais de TI](#it-professionals)
-   [Desenvolvedores de infraestrutura](#infrastructure-developers)

esta documentação destina-se a desenvolvedores de software que desejam criar aplicativos que usam Windows Installer. Como a principal fonte de material de referência para o instalador, o SDK fornece informações sobre pacotes de instalação e o serviço do instalador. Ele contém descrições completas da API (interface de programação de aplicativo) e dos elementos do banco de dados do instalador.

para obter mais informações, consulte [outras fontes de Windows Installer informações](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Desenvolvedores de aplicativos

os desenvolvedores de aplicativos criam aplicativos que chamam a interface de programação de aplicativo Windows Installer e instalam Windows pacotes do instalador em tempo de execução. o Windows Installer pode funcionar em um aplicativo como o autoreparo e a instalação sob demanda. Normalmente, os desenvolvedores de aplicativos fazem o seguinte:

-   Habilite a instalação sob demanda de aplicativos em tempo de execução de dentro de outro aplicativo.

    Para saber mais, consulte o seguinte:

    -   [Usando funções do instalador](using-installer-functions.md)
    -   [Referência de função do instalador](installer-function-reference.md)
    -   [Instalação sob demanda](installation-on-demand.md)
    -   [Gerenciamento de componentes](component-management.md)
    -   [Editando atalhos do instalador](editing-installer-shortcuts.md)
    -   [**Propriedade OLEAdvtSupport**](oleadvtsupport.md)
    -   [Suporte de plataforma do anúncio](platform-support-of-advertisement.md)

-   Habilite o reparo automático de aplicativos reinstalando os componentes conforme necessário no tempo de execução.

    Para saber mais, consulte o seguinte:

    -   [Usando funções do instalador](using-installer-functions.md)
    -   [Referência de função do instalador](installer-function-reference.md)
    -   [Resiliência](resiliency.md)
    -   [Resiliência de origem](source-resiliency.md)
    -   [Pesquisando um componente ou recurso desfeito](searching-for-a-broken-feature-or-component.md)
    -   [Substituindo arquivos existentes](replacing-existing-files.md)

-   Exiba uma interface do usuário para coletar informações de usuário e preferências de configuração na primeira vez que um aplicativo for instalado ou executado. a interface do usuário deve ser adicionada pelo autor da instalação do pacote de Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [Usando funções do instalador](using-installer-functions.md)
    -   [Inicializando um aplicativo](initializing-an-application.md)
    -   [Caixa de diálogo FirstRun](firstrun-dialog.md)
    -   [Sobre a interface do usuário](about-the-user-interface.md)

-   Crie aplicativos que usam um modelo de indireção para se referir a componentes com funcionalidade paralela. as categorias de componentes qualificados devem ser adicionadas pelo autor da instalação do pacote de Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [Componentes qualificados](qualified-components.md)
    -   [Usando componentes qualificados](using-qualified-components.md)

-   Use assemblies privados e lado a lado para isolar aplicativos e reduzir conflitos de DLL.

    Para saber mais, consulte o seguinte:

    -   [Assemblies](assemblies.md)
    -   [chaves do registro de Assembly gravadas por Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [instalando Assemblies do Win32 para compartilhamento lado a lado no Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [instalando Assemblies do Win32 para o uso particular de um aplicativo no Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [Tabela MsiAssembly](msiassembly-table.md)
    -   [Tabela MsiAssemblyName](msiassemblyname-table.md)
    -   [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**Propriedade MsiWin32AssemblySupport**](msiwin32assemblysupport.md)
    -   [**Propriedade MsiNetAssemblySupport**](msinetassemblysupport.md)
    -   [**Componentes isolados**](isolated-components.md)

-   Prepare o aplicativo para instalar suas próprias atualizações importantes abrangentes.

    Para saber mais, consulte o seguinte:

    -   [Aplicação de patch e atualizações](patching-and-upgrades.md)
    -   [Principais atualizações](major-upgrades.md)
    -   [**Propriedade UpgradeCode**](upgradecode.md)
    -   [**Usando um UpgradeCode**](using-an-upgradecode.md)
    -   [Impedindo que um pacote antigo seja instalado em uma versão mais recente](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Prepare o aplicativo para instalar suas próprias atualizações secundárias, pequenas atualizações ou correções.

    Para saber mais, consulte o seguinte:

    -   [Aplicação de patch e atualizações](patching-and-upgrades.md)
    -   [Pequenas atualizações](small-updates.md)
    -   [Atualizações secundárias](minor-upgrades.md)

-   Organize os recursos do aplicativo em componentes que podem funcionar com o Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [Windows Componentes do instalador](windows-installer-components.md)
    -   [Trabalhando com recursos e componentes](working-with-features-and-components.md)
    -   [Usando componentes transitivos](using-transitive-components.md)
    -   [O que acontece se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organizando aplicativos em componentes](organizing-applications-into-components.md)
    -   [Componentes isolados](isolated-components.md)
    -   [Componentes qualificados](qualified-components.md)

## <a name="setup-authors"></a>Autores de instalação

os autores de instalação criam pacotes de Windows Installer (arquivos de .msi) que contêm a lógica de instalação e as informações necessárias para instalar um aplicativo. normalmente, eles usam ferramentas de criação como [Orca.exe](orca-exe.md) para popular o banco de dados de Windows Installer com a lógica de instalação e as informações. Normalmente, os autores da instalação fazem o seguinte:

-   Determine a funcionalidade disponível com diferentes versões de Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [determinando a versão de Windows Installer](determining-the-windows-installer-version.md)
    -   [versões lançadas do Windows Installer](released-versions-of-windows-installer.md)
    -   [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md)

-   Organize os recursos do aplicativo em Windows Installer componentes.

    Para saber mais, consulte o seguinte:

    -   [Windows Componentes do instalador](windows-installer-components.md)
    -   [Organizando aplicativos em componentes](organizing-applications-into-components.md)
    -   [Alterando o código do componente](changing-the-component-code.md)
    -   [O que acontece se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows Exemplos de instalador](windows-installer-examples.md)

-   Use ferramentas de criação de pacote Windows Installer de terceiros ou ferramentas de SDK, como [Orca.exe](orca-exe.md) para popular um banco de dados de instalação e criar um pacote de Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
    -   [Pacote de instalação, sobre o banco de dados do instalador](installation-package.md)
    -   [Windows Extensões de arquivo do instalador](windows-installer-file-extensions.md)
    -   [Tabelas de banco de dados](database-tables.md)
    -   [Códigos de pacote](package-codes.md)
    -   [Como autor de um pacote grande](authoring-a-large-package.md)
    -   [Windows Instalador em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Nomeando tabelas, propriedades e ações personalizadas](naming-custom-tables-properties-and-actions.md)
    -   [Limitações do OLE Fluxos](ole-limitations-on-streams.md)
    -   [Formato de definição de coluna](column-definition-format.md)
    -   [Reduzindo o tamanho de um .msi arquivo](reducing-the-size-of-an--msi-file.md)

-   Autor do banco de Windows instalador para instalar arquivos.

    Para saber mais, consulte o seguinte:

    -   [Grupo de Tabelas Principais](core-tables-group.md)
    -   [Grupo tabelas de arquivos](file-tables-group.md)
    -   [File Table](file-table.md)
    -   [Pesquisa de arquivos](file-searching.md)
    -   [Custo do arquivo](file-costing.md)
    -   [Instalação de arquivo](file-installation.md)
    -   [Arquivos de adoção](companion-files.md)
    -   [Regras de versão de arquivo](file-versioning-rules.md)
    -   [Versão do arquivo padrão](default-file-versioning.md)
    -   [Substituindo arquivos existentes](replacing-existing-files.md)
    -   [Usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md)
    -   [Removendo arquivos desaparados](removing-stranded-files.md)
    -   [Instalando componentes permanentes, arquivos, fontes, chaves do Registro](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Tabela FileSFPCatalog](filesfpcatalog-table.md)
    -   [Pesquisando um arquivo e criando uma propriedade que mantém o caminho do arquivo](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Pesquisando um diretório e um arquivo no diretório](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows Exemplos do instalador](windows-installer-examples.md)

-   Autor de um Windows de dados do Instalador que instala uma estrutura e pastas de diretório.

    Para saber mais, consulte o seguinte:

    -   [Grupo de Tabelas Principais](core-tables-group.md)
    -   [Grupo tabelas de arquivos](file-tables-group.md)
    -   [Tabela de componentes](component-table.md)
    -   [Tabela de diretórios](directory-table.md)
    -   [Usando a tabela de diretório](using-the-directory-table.md)
    -   [Usando uma propriedade de diretório em um caminho](using-a-directory-property-in-a-path.md)
    -   [Propriedades da pasta do sistema](property-reference.md)
    -   [Tabela CreateFolder](createfolder-table.md)
    -   [Tabela LockPermissions](lockpermissions-table.md)
    -   [Tabela MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)
    -   [Windows Exemplos do instalador](windows-installer-examples.md)

-   Cria um banco Windows instalador de dados que instala chaves do Registro.

    Para saber mais, consulte o seguinte:

    -   [Grupo de Tabelas Principais](core-tables-group.md)
    -   [Grupo de Tabelas do Registro](registry-tables-group.md)
    -   [Tabela do Registro](registry-table.md)
    -   [Modificando o Registro](modifying-the-registry.md)
    -   [Adicionando ou removendo chaves do Registro na instalação ou remoção de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no Registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Instalando componentes permanentes, arquivos, fontes, chaves do Registro](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Pesquisando aplicativos, arquivos, entradas do Registro ou .ini de arquivo existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Pesquisando uma entrada do Registro e criando uma propriedade que mantém o valor do Registro](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Chaves do Registro de Assembly escritas pelo instalador Windows assembly](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Desinstalar a chave do Registro](uninstall-registry-key.md)
    -   [Tabela SelfReg](selfreg-table.md)
    -   [Especificando a ordem de auto-registro](specifying-the-order-of-self-registration.md)
    -   [Windows Exemplos do instalador](windows-installer-examples.md)

-   Autor de um Windows instalador de dados que instala serviços.

    Para saber mais, consulte o seguinte:

    -   [Tabela ServiceInstall](serviceinstall-table.md)
    -   [Tabela ServiceControl](servicecontrol-table.md)
    -   [Tabela de componentes](component-table.md)

-   Autor de um Windows instalador que instala componentes isolados ou componentes COM.

    Para saber mais, consulte o seguinte:

    -   [Grupo de Tabelas do Registro](registry-tables-group.md)
    -   [Tabela de classes](class-table.md)
    -   [Tabela complus](complus-table.md)
    -   [Componentes isolados](isolated-components.md)
    -   [Usando componentes isolados](using-isolated-components.md)
    -   [Instalação de componentes isolados](installation-of-isolated-components.md)
    -   [Reinstalação de componentes isolados](reinstallation-of-isolated-components.md)
    -   [Remoção de componentes isolados](removal-of-isolated-components.md)
    -   [Instalando um componente COM em um local privado](installing-a-com-component-to-a-private-location.md)
    -   [Tornar um componente COM em um pacote existente privado](make-a-com-component-in-an-existing-package-private.md)
    -   [Instalando um aplicativo COM+ com o Windows Instalador](installing-a-com--application-with-the-windows-installer.md)
    -   [Instalando um componente não COM em um local privado](installing-a-non-com-component-to-a-private-location.md)
    -   [Tornar um componente não COM em um pacote existente privado](make-a-non-com-component-in-an-existing-package-private.md)

-   Autor de um Windows instalador de dados que instala assemblies.

    Para saber mais, consulte o seguinte:

    -   [Tabela MsiAssembly](msiassembly-table.md)
    -   [Tabela MsiAssemblyName](msiassemblyname-table.md)
    -   [Assemblies](assemblies.md)
    -   [Chaves do Registro de Assembly escritas pelo instalador Windows assembly](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Instalação de assemblies Win32](installation-of-win32-assemblies.md)

-   Autor de um Windows instalador de dados que instala drivers e tradutores ODBC.

    Para saber mais, consulte o seguinte:

    -   [Tabela ODBCAttribute](odbcattribute-table.md)
    -   [Tabela ODBCDriver](odbcdriver-table.md)
    -   [Tabela ODBCTranslator](odbctranslator-table.md)
    -   [Tabela ODBCDataSource](odbcdatasource-table.md)
    -   [Tabela ODBCSourceAttribute](odbcsourceattribute-table.md)

-   Autor de um Windows instalador de dados que instala o MIME.

    Para saber mais, consulte o seguinte:

    -   [Tabela MIME](mime-table.md)
    -   [Tabela de extensão](extension-table.md)
    -   [Modificando o Registro](modifying-the-registry.md)

-   Autor de um banco Windows instalador que instala variáveis de ambiente.

    Para saber mais, consulte o seguinte:

    -   [Tabela de ambiente](environment-table.md)

-   crie um banco de dados Windows Installer que instala atalhos.

    Para saber mais, consulte o seguinte:

    -   [Tabela de atalho](shortcut-table.md)
    -   [Tabela MsiShortcutProperty](msishortcutproperty-table.md)
    -   [Editando atalhos do instalador](editing-installer-shortcuts.md)
    -   [Windows Exemplos de instalador](windows-installer-examples.md)

-   crie um banco de dados Windows Installer que instala várias instâncias de aplicativos.

    Para saber mais, consulte o seguinte:

    -   [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md)
    -   [Criando várias instâncias com transformações de instância](authoring-multiple-instances-with-instance-transforms.md)
    -   [Instalando várias instâncias com transformações de instância](installing-multiple-instances-with-instance-transforms.md)

-   Especifique opções e Estados de seleção de recursos padrão.

    Para saber mais, consulte o seguinte:

    -   [Grupo de tabelas principais](core-tables-group.md)
    -   [Tabela de componentes](component-table.md)
    -   [Tabela de recursos](feature-table.md)
    -   [Tabela FeatureComponents](featurecomponents-table.md)
    -   [Controlando Estados de seleção de recursos](controlling-feature-selection-states.md)
    -   [Propriedades de opções de instalação de recurso](property-reference.md)

-   Especifique as condições que devem ser atendidas para instalar um aplicativo ou componentes selecionados.

    Para saber mais, consulte o seguinte:

    -   [Tabela de condição](condition-table.md)
    -   [Tabela LaunchCondition](launchcondition-table.md)
    -   [Tabela de componentes](component-table.md)
    -   [Usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md)
    -   [Sintaxe de instrução condicional](conditional-statement-syntax.md)
    -   [Ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md)
    -   [Exemplos de sintaxe de instrução condicional](examples-of-conditional-statement-syntax.md)

-   Crie a sequência de ações usadas para instalar o aplicativo.

    Para saber mais, consulte o seguinte:

    -   [Usando uma tabela de sequência](using-a-sequence-table.md)
    -   [Grupo de tabelas de procedimento de instalação](installation-procedure-tables-group.md)
    -   [Exemplo detalhado da tabela de sequência](sequence-table-detailed-example.md)
    -   [Ações com restrições de sequenciamento](actions-with-sequencing-restrictions.md)
    -   [Ações sem restrições de sequenciamento](actions-without-sequencing-restrictions.md)
    -   [Usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md)
    -   [Sintaxe de instrução condicional](conditional-statement-syntax.md)
    -   [Exemplos de sintaxe de instrução condicional](examples-of-conditional-statement-syntax.md)
    -   [Ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md)
    -   [Ações padrão](standard-actions.md)
    -   [Windows Exemplos de instalador](windows-installer-examples.md)

-   Prepare o pacote de instalação do aplicativo para atualizações futuras do aplicativo pelo serviço de Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [Aplicação de patch e atualizações](patching-and-upgrades.md)
    -   [Preparando um aplicativo para atualizações principais futuras](preparing-an-application-for-future-major-upgrades.md)
    -   [Usando um UpgradeCode](using-an-upgradecode.md)
    -   [Atualizar tabela](upgrade-table.md)
    -   [**Propriedade UpgradeCode**](upgradecode.md)
    -   [Impedindo que um pacote antigo seja instalado em uma versão mais recente](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Alterando o código do produto](changing-the-product-code.md)
    -   [Atualizando assemblies](updating-assemblies.md)
    -   [Windows Exemplos de instalador](windows-installer-examples.md)

-   solucionar problemas Windows Installer pacotes em desenvolvimento.

    Para saber mais, consulte o seguinte:

    -   [Validação do pacote](package-validation.md)
    -   [Avaliadores de consistência internos-ICEs](internal-consistency-evaluators-ices.md)
    -   [Windows Log do instalador](windows-installer-logging.md)
    -   [Verificando a instalação de recursos, componentes, arquivos](checking-the-installation-of-features-components-files.md)
    -   [Criando um pacote grande](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Windows Ferramentas de desenvolvimento do instalador](windows-installer-development-tools.md)
    -   [Validando módulos de mesclagem](validating-merge-modules.md)
    -   [Validando um banco de dados de instalação](validating-an-installation-database.md)
    -   [Validando uma atualização de instalação](validating-an-installation-upgrade.md)
    -   [Pesquisando um componente ou recurso desfeito](searching-for-a-broken-feature-or-component.md)
    -   [Windows Mensagens de erro do instalador](windows-installer-error-messages.md)
    -   [Registro em log de solicitações de reinicialização](logging-of-reboot-requests.md)

-   Garanta uma instalação e instalação seguras do aplicativo.

    Para saber mais, consulte o seguinte:

    -   [Diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md)
    -   [Diretrizes para proteger ações personalizadas](guidelines-for-securing-custom-actions.md)
    -   [Segurança de ação personalizada](custom-action-security.md)
    -   [Diretrizes para proteger pacotes em computadores bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Criando uma instalação assinada totalmente verificada usando a automação](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [Um exemplo de instalação do Windows Installer baseado em URL](a-url-based-windows-installer-installation-example.md)
    -   [Criando a interface do usuário para entrada de senha](authoring-the-user-interface-for-password-input.md)
    -   [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md)
    -   [usando Windows Installer com o UAC](using-windows-installer-with-uac.md)
    -   [Aplicação de patch de UAC (controle de conta de usuário)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**Propriedade AdminUser**](adminuser.md)
    -   [**Propriedade privilegiada**](privileged.md)
    -   [**Propriedade SecureCustomProperties**](securecustomproperties.md)

-   Crie uma interface do usuário para apresentar opções para configurar a instalação e obter informações do usuário sobre o processo de instalação pendente.

    Para saber mais, consulte o seguinte:

    -   [Sobre a interface do usuário](about-the-user-interface.md)
    -   [Adicionando controles e texto](adding-controls-and-text.md)
    -   [Criando um controle ProgressBar](authoring-a-progressbar-control.md)
    -   [Criando mensagens de prompt de disco](authoring-disk-prompt-messages.md)
    -   [Criando uma condicional "Aguarde..." Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md)
    -   [Visualizando a interface do usuário](previewing-the-user-interface.md)
    -   [Adicionando texto armazenado em uma propriedade](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Crie uma interface de usuário externa para apresentar uma interface de usuário personalizada para configurar a instalação e obter informações do usuário sobre o processo de instalação pendente.

    Para saber mais, consulte o seguinte:

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Monitorando uma instalação usando o MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [analisando mensagens de Windows Installer](parsing-windows-installer-messages.md)
    -   [Retornando valores de um manipulador de interface do usuário externo](returning-values-from-an-external-user-interface-handler.md)
    -   [MANIPULADOR \_ INSTALLUI](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Manipulando mensagens de progresso usando MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md)
    -   [Monitorando uma instalação usando MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md)

-   Definir informações para o aplicativo em **Adicionar/Remover Programas** (ARP).)

    Para saber mais, consulte o seguinte:

    -   [Configurando Adicionar/Remover Programas com Windows Instalador](configuring-add-remove-programs-with-windows-installer.md)
    -   [Adicionando e removendo um aplicativo e não deixando nenhum rastreamento no Registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Desinstalar a chave do Registro](uninstall-registry-key.md)

-   Escreva ações personalizadas para lidar com a lógica de instalação que não tem suporte nativo do Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [Ações personalizadas](custom-actions.md)
    -   [Lista resumida de todos os tipos de ação personalizados](summary-list-of-all-custom-action-types.md)
    -   [Diretrizes para proteger ações personalizadas](guidelines-for-securing-custom-actions.md)
    -   [Referência de ação personalizada](custom-action-reference.md)
    -   [Usando uma ação personalizada para criar contas de usuário em um computador local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Usando uma ação personalizada para iniciar um arquivo instalado no final da instalação](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Acessando um banco de dados ou sessão de dentro de uma ação personalizada](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Acessando a sessão do instalador atual de dentro de uma ação personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Alterando o estado do sistema usando uma ação personalizada](changing-the-system-state-using-a-custom-action.md)

-   Inicializar o Windows instalador no computador de um usuário.

    Para saber mais, consulte o seguinte:

    -   [Inicialização](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Inicialização de download da Internet](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [Um exemplo de instalação do Windows Installer baseado em URL](a-url-based-windows-installer-installation-example.md)
    -   [Configurando os recursos Setup.exe dados](configuring-the-setup-exe-resources.md)
    -   [Baixando uma instalação da Internet](downloading-an-installation-from-the-internet.md)

-   Adera Acessibilidade Ativa diretrizes ao escrever Windows do Instalador.

    Para saber mais, consulte o seguinte:

    -   [Acessibilidade](accessibility.md)

-   Prepare-se para a internacionalização de uma configuração de aplicativo.

    Para saber mais, consulte o seguinte:

    -   [Preparando um pacote Windows instalador para localização,](preparing-a-windows-installer-package-for-localization.md)
    -   [Localizando um Windows instalador de dados](localizing-a-windows-installer-package.md)
    -   [Tratamento de página de código (Windows instalador)](code-page-handling-windows-installer-.md)
    -   [Adicionando recursos localizados](adding-localized-resources.md)
    -   [Um exemplo de localização](a-localization-example.md)
    -   [Localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md)
    -   [Localizando colunas de banco de dados](localizing-database-columns.md)
    -   [Criando um banco de dados com uma página de código neutro](creating-a-database-with-a-neutral-code-page.md)
    -   [Manipulação de página de código de tabelas importadas e exportadas](code-page-handling-of-imported-and-exported-tables.md)
    -   [Localizando o idioma exibido por diálogos](localizing-the-language-displayed-by-dialogs.md)
    -   [Importando tabelas de Erro Localizado e ActionText](importing-localized-error-and-actiontext-tables.md)
    -   [Atualizando as propriedades ProductLanguage e ProductCode](updating-productlanguage-and-productcode-properties.md)
    -   [Atualizando um fluxo de informações de resumo](updating-a-summary-information-stream.md)
    -   [Componentes qualificados](qualified-components.md)
    -   [Tabela UIText](uitext-table.md)
    -   [Gerenciar idioma e página de código](manage-language-and-codepage.md)
    -   [Verificando a página de código do banco de dados de instalação](checking-the-installation-database-code-page.md)

-   Crie Windows pacotes do Instalador para plataformas de 32 bits e 64 bits.

    Para saber mais, consulte o seguinte:

    -   [Windows Instalador em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Ações personalizadas de 64 bits](64-bit-custom-actions.md)
    -   [Usando ações personalizadas de 64 bits](using-64-bit-custom-actions.md)
    -   [Usando módulos de mesclagem de 64 bits](using-64-bit-merge-modules.md)

-   Redistribua componentes Windows instalador compartilhados e a lógica de instalação como módulos de mesclagem.

    Para saber mais, consulte o seguinte:

    -   [Mesclar módulos](merge-modules.md)
    -   [Como fazer uma transformação de linguagem para um módulo de mesclagem de vários idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Aplicando um módulo de mesclagem configurável com personalizações](applying-a-configurable-merge-module-with-customizations.md)

-   Agendar ou suprimir reinicializações durante uma Windows instalação do instalador.

    Para saber mais, consulte o seguinte:

    -   [Reinicializações do sistema](system-reboots.md)
    -   [Registro em log de solicitações de reinicialização](logging-of-reboot-requests.md)

-   Crie atualizações ou correções para um aplicativo existente criando um patch.

    Para saber mais, consulte o seguinte:

    -   [Criando um pequeno patch de atualização](creating-a-small-update-patch.md)
    -   [Um pequeno exemplo de a patch de atualização](a-small-update-patching-example.md)

-   Autor de um pacote de finalidade dupla capaz de instalar um aplicativo apenas para o usuário atual ou para todos os usuários do computador.

    Para saber mais, consulte o seguinte:

    -   [Contexto de instalação](installation-context.md)
    -   [Autorização de pacote único](single-package-authoring.md)
    -   [Exemplo de autor de pacote único](single-package-authoring-example.md)

-   Personalize os serviços no computador usando o Windows Instalador.

    Para saber mais, consulte o seguinte:

    -   [Usando a configuração de serviços](using-services-configuration.md)

-   Proteja recursos no computador usando o Windows Instalador.

    Para saber mais, consulte o seguinte:

    -   [Diretrizes para a autorização de instalações seguras](guidelines-for-authoring-secure-installations.md)
    -   [Proteger recursos](securing-resources-.md)

-   Enumerar todos os componentes instalados no computador e obter o caminho da chave para o componente.

    Para saber mais, consulte o seguinte:

    -   [Enumerando componentes](enumerating-components-.md)

-   Instale vários pacotes usando [*o processamento de transações*](t-gly.md).

    Para saber mais, consulte o seguinte:

    -   [Instalações de vários pacotes](multiple-package-installations.md)

-   Inserir uma interface do usuário personalizada no pacote Windows Instalador.

    Para saber mais, consulte o seguinte:

    -   [Usando a interface do usuário](using-the-user-interface.md)
    -   [Usando uma interface do usuário inserida](using-an-embedded-ui.md)

## <a name="it-professionals"></a>Profissionais de TI

Os profissionais e administradores de TI personalizam e implantam pacotes Windows instalador existentes. Esses usuários reempacodam as configurações para aplicativos existentes em pacotes de instalação Windows Instalador e instalam e mantêm imagens administrativas de instalações do Windows Instalador em redes.

-   Personalizar aplicativos e configuração gerando e aplicando Windows do Instalador

    Para saber mais, consulte o seguinte:

    -   [Personalização](customization.md)
    -   [Transformações de banco de dados](database-transforms.md)
    -   [Um exemplo de transformação de personalização](a-customization-transform-example.md)
    -   [Mesclagem e transformação](merges-and-transforms.md)
    -   [Usando transformações para adicionar recursos](using-transforms-to-add-resources.md)
    -   [Gerar uma transformação](generate-a-transform.md)
    -   [Opções de linha de comando](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Aplicar uma transformação](apply-a-transform.md)
    -   [Exibir uma transformação](view-a-transform.md)
    -   [Exibir diferenças entre dois bancos de dados](view-differences-between-two-databases.md)
    -   [Aplicação de patch em aplicativos personalizados](patching-customized-applications.md)

-   implante um pacote de instalação Windows Installer, atualização ou patch.

    Para saber mais, consulte o seguinte:

    -   [Instalando um aplicativo](installing-an-application.md)
    -   [Aplicação de patch e atualizações](patching-and-upgrades.md)
    -   [Transformações](transforms.md)
    -   [Instalando um pacote com privilégios elevados para um não administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Aplicando as principais atualizações por meio da aplicação de patch na instalação local do produto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicando as principais atualizações instalando o produto](applying-major-upgrades-by-installing-the-product.md)
    -   [Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicação de patch nas instalações iniciais](patching-initial-installations.md)
    -   [Opções de linha de comando](command-line-options.md)

-   solucionar problemas de pacotes Windows Installer.

    Para saber mais, consulte o seguinte:

    -   [Windows Log do instalador](windows-installer-logging.md)
    -   [Verificando a instalação de recursos, componentes, arquivos](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Pesquisando um componente ou recurso desfeito](searching-for-a-broken-feature-or-component.md)
    -   [Windows Mensagens de erro do instalador](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   Use scripts para consultar Windows Installer pacotes para obter informações sobre um produto e modificar a instalação.

    Para saber mais, consulte o seguinte:

    -   [Interface de automação](automation-interface.md)
    -   [Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
    -   [usando Windows Installer com WMI](using-windows-installer-with-wmi.md)

-   Crie e mantenha instalações administrativas.

    Para saber mais, consulte o seguinte:

    -   [Instalação administrativa](administrative-installation.md)
    -   [Opções de linha de comando](command-line-options.md)
    -   [**Propriedade adminproperties**](adminproperties.md)
    -   [Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicando um pacote de patch a uma instalação administrativa](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Ordem de execução da ação](action-execution-order.md)
    -   [**Propriedade IsAdminPackage**](isadminpackage.md)
    -   [Ordem de precedência de propriedade](order-of-property-precedence.md)
    -   [**Propriedade adminproperties**](adminproperties.md)

-   Disponibilizar um aplicativo para todos os usuários de um computador ou apenas para um usuário especificado.

    Para saber mais, consulte o seguinte:

    -   [Contexto de instalação](installation-context.md)
    -   [**Propriedade ALLUSERS**](allusers.md)

-   Interprete pacotes, instale produtos e configure opções de recursos usando uma linha de comando.

    Para saber mais, consulte o seguinte:

    -   [Opções de linha de comando](command-line-options.md)
    -   [Definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md)
    -   [Obtendo e definindo propriedades](getting-and-setting-properties.md)
    -   [Reinstalando um recurso ou aplicativo](reinstalling-a-feature-or-application.md)
    -   [Aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)
    -   [Aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicando as principais atualizações instalando o produto](applying-major-upgrades-by-installing-the-product.md)
    -   [Propriedades de configuração](property-reference.md)
    -   [Propriedades de opções de instalação de recurso](property-reference.md)

-   Trabalhe com a política para gerenciar direitos de acesso e permissões.

    Para saber mais, consulte o seguinte:

    -   [Políticas de máquina](machine-policies.md),
    -   [Políticas de usuário](user-policies.md),
    -   [Instalando um pacote com privilégios elevados para um não administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anunciando um aplicativo Per-User para ser instalado com privilégios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Usando uma ação personalizada para criar contas de usuário em um computador local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Propriedade AdminUser**](adminuser.md)
    -   [**Propriedade privilegiada**](privileged.md)
    -   [**Propriedade EnableUserControl**](enableusercontrol.md)
    -   [**Propriedade UserID**](usersid.md)
    -   [**Propriedade SecureCustomProperties**](securecustomproperties.md)

-   Instale vários pacotes usando o [*processamento de transações*](t-gly.md).

    Para saber mais, consulte o seguinte:

    -   [Instalações de vários pacotes](multiple-package-installations.md)

-   inserir uma interface do usuário personalizada em um pacote Windows Installer..

    Para saber mais, consulte o seguinte:

    -   [Usando a interface do usuário](using-the-user-interface.md)
    -   [Usando uma interface do usuário inserida](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Desenvolvedores de infraestrutura

os desenvolvedores de infraestrutura podem criar plataformas unificadas para a implantação e o gerenciamento de software que usa o serviço de Windows Installer. eles podem usar a interface de programação de Windows Installer para consultar, gerenciar e distribuir aplicativos, patches e fontes em um sistema.

-   Localize, inventaria e consulte o estado, as informações e os clientes dos componentes.

    Para saber mais, consulte o seguinte:

    -   [Funções específicas do componente](installer-function-reference.md)
    -   [Funções de status do sistema](installer-function-reference.md)
    -   [Objeto do instalador](installer-object.md)
    -   [Objeto Product](product-object.md)
    -   [Objeto patch](patch-object.md)

-   Inventário e consulta de informações e o estado dos produtos e recursos.

    Para saber mais, consulte o seguinte:

    -   [Produtos e patches de inventário](inventory-products-and-patches-.md)
    -   [Funções de status do sistema](installer-function-reference.md)
    -   [Funções de consulta de produto](installer-function-reference.md)
    -   [Objeto do instalador](installer-object.md)
    -   [Objeto Product](product-object.md)
    -   [Objeto patch](patch-object.md)

-   melhore a resiliência da origem usando o Windows Installer para inventariar, consultar e modificar a lista de origem de aplicativos, atualizações e patches.

    Para saber mais, consulte o seguinte:

    -   [**Propriedade SOURCELIST**](sourcelist.md)
    -   [**Resiliência de origem**](source-resiliency.md)
    -   [Funções de instalação e configuração](installer-function-reference.md)
    -   [Objeto installer](installer-object.md)
    -   [Objeto Product](product-object.md)
    -   [Objeto Patch](patch-object.md)

-   Melhore a resiliência de origem usando o instalador Windows para inventariar, consultar e modificar fontes de mídia.

    Para saber mais, consulte o seguinte:

    -   [**Propriedade SOURCELIST**](sourcelist.md)
    -   [Resiliência de origem](source-resiliency.md)
    -   [Funções de instalação e configuração](installer-function-reference.md)
    -   [Objeto Product](product-object.md)
    -   [Objeto Patch](patch-object.md)

-   Inventário e consulta para obter informações e o estado dos patches.

    Para saber mais, consulte o seguinte:

    -   [Produtos e patches de inventário](inventory-products-and-patches-.md)
    -   [Referência de função do instalador](installer-function-reference.md)
    -   [Objeto Patch](patch-object.md)

-   Trabalhe com a política para gerenciar direitos de acesso e permissões.

    Para saber mais, consulte o seguinte:

    -   [Políticas de computador](machine-policies.md)
    -   [Políticas de usuário](user-policies.md)
    -   [Instalando um pacote com privilégios elevados para um não administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anunciando um Per-User aplicativo a ser instalado com privilégios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Usando uma ação personalizada para criar contas de usuário em um computador local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Propriedade AdminUser**](adminuser.md)
    -   [**Propriedade Privileged**](privileged.md)
    -   [**Propriedade EnableUserControl**](enableusercontrol.md)
    -   [**Propriedade UserSID**](usersid.md)
    -   [**Propriedade SecureCustomProperties**](securecustomproperties.md)

 

 



