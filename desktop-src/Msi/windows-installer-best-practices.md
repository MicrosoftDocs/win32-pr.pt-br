---
description: 'Esta seção enumera uma lista de dicas, vinculada à documentação principal do SDK do instalador do Windows, para ajudar desenvolvedores de aplicativos, criadores de instalação, profissionais de TI e desenvolvedores de infraestrutura a descobrir práticas recomendadas para usar o instalador Windows:'
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Windows Práticas recomendadas do instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e430cf8871279e18107b3ab1deb1f347e9d4779b619ab6cf8133d30cdfa4ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808956"
---
# <a name="windows-installer-best-practices"></a>Windows Práticas recomendadas do instalador

Esta seção enumera uma lista de dicas, vinculada à documentação principal do SDK do instalador do Windows, para ajudar desenvolvedores de aplicativos, criadores de instalação, profissionais de TI e desenvolvedores de infraestrutura a descobrir práticas recomendadas para usar o instalador Windows:

-   [Atualize a Windows do instalador.](#update-the-windows-installer-version)
-   [Atender aos requisitos Windows de certificação de logotipo.](#meet-the-windows-logo-certification-requirements)
-   [Prepare o pacote para localização.](#prepare-the-package-for-localization)
-   [Atualize a documentação e Windows ferramentas de desenvolvimento do instalador do Windows.](#update-your-windows-installer-development-tools-and-documentation)
-   [Se você decidir reempacodar um aplicativo de instalação herdado, siga as boas práticas de reempacodagem.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [Não tente substituir recursos protegidos.](#do-not-try-to-replace-protected-resources)
-   [Não dependa de recursos não críticos.](#do-not-depend-upon-non-critical-resources)
-   [Use a API para recuperar informações Windows configuração do Instalador.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organize a instalação do aplicativo em torno dos componentes.](#organize-the-installation-of-your-application-around-components)
-   [Reduza o tamanho de pacotes Windows instalador grandes.](#reduce-the-size-of-large-windows-installer-packages)
-   [Se você usar ações personalizadas, siga as boas práticas de ação personalizadas.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Se você usar assemblies, siga as boas práticas de assembly](#if-you-use-assemblies-follow-good-assembly-practices)
-   [Não enviar instalações simultâneas.](#do-not-ship-concurrent-installations)
-   [Mantenha os nomes de pacote e os códigos de pacote consistentes.](#keep-package-names-and-package-codes-consistent)
-   [Não use as tabelas SelfReg e TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Forneça a opção de instalação sem uma interface do usuário.](#provide-the-option-to-install-without-a-user-interface)
-   [Evite usar a política AlwaysInstallElevated.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Habilita a política DisableMedia para limitar a instalação não autorizada.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Mantenha os arquivos de origem do pacote original seguros e disponíveis para os usuários.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Habilita o log detalhado no computador do usuário ao solucionar problemas de implantação.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [A desinstalação deixa o computador do usuário em um estado limpo.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Testar pacotes para implantação de instalação por usuário e por computador.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Planeje e teste uma estratégia de manutenção antes de enviar o aplicativo.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Reduza a dependência de atualizações nas fontes originais.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [Não distribua módulos de mesclagem insserviços.](#do-not-distribute-unserviceable-merge-modules)
-   [Evite a adoção de patches de instalações administrativas.](#avoid-patching-administrative-installations)
-   [Registre atualizações para executar com privilégios elevados.](#register-updates-to-run-with-elevated-privilege)
-   [Use a Tabela MsiPatchSequence para sequenciar patches.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Teste o pacote de instalação completamente.](#test-the-installation-package-thoroughly)
-   [Corrige todos os erros de validação antes de implantar um pacote de instalação novo ou revisado.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Autor de uma instalação segura.](#author-a-secure-installation)
-   [Usar PMSIHANDLE em vez de HANDLE](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Atualize a Windows do instalador.

-   Use Windows Installer 5.0 no Windows Server 2008 R2 e Windows 7. Essa é a Windows do instalador fornecida com o sistema operacional.
-   Use o Windows Installer 4.5 no Windows Server 2008, Windows Server 2003 com Service Pack 1 (SP1), Windows Vista com Service Pack 1 (SP1) ou Windows XP com Service Pack 2 (SP2). Para obter informações sobre como obter a versão Windows mais recente do Instalador, [consulte Windows Installer Redistributables](windows-installer-redistributables.md).
-   Use Windows Instalador 3.1 no Windows 2000 com o Service Pack 3 (SP3). Windows O instalador versão 3.1 tem recursos que facilitam a melhor manutenção e aplicação [de patch de aplicativos.](patching.md)
-   Muitos recursos importantes foram introduzidos com a versão 3.0 e estão listados na seção Sem suporte no [Windows Installer Versão 2.0](not-supported-in-windows-installer-version-2-0.md). Pacotes de instalação e atualizações criados para o Windows Installer 2.0 podem ser instalados usando o Windows Installer 3.0 e posterior. Pacotes de patch que contêm as novas tabelas usadas pelo Windows Installer 3.0 ainda podem ser aplicados usando versões anteriores do Instalador do Windows, mas sem a funcionalidade de aplicação de patch do Windows Installer 3.0. Também é possível autor de patches que exigem explicitamente o Windows Installer 3.0 que não pode ser aplicado por versões anteriores do Windows Installer. Se um usuário não puder atualizar a versão do instalador, verifique se o aplicativo ou a atualização será compatível com uma atualização futura do Windows Installer.
-   Para ver uma lista dos recursos Windows Instalador do Windows não suportados por versões anteriores do instalador do Windows, consulte Novidades no [Windows Installer](what-s-new-in-windows-installer.md).

## <a name="meet-the-windows-logo-certification-requirements"></a>Atender aos requisitos Windows de certificação de logotipo.

-   Mesmo que você não pretenda enviar seu aplicativo para o programa de logotipo, seguir as diretrizes de certificação de logotipo pode ajudar a melhorar o pacote Windows Instalador. Para ter uma visão geral dos requisitos de logotipo e links para programas de certificação de logotipo específicos, consulte Windows Instalador e [Requisitos de Logotipo.](windows-installer-and-logo-requirements.md)

## <a name="prepare-the-package-for-localization"></a>Prepare o pacote para localização.

-   É uma boa prática se preparar para a localização futura ao autorizar o pacote de instalação original. Você pode seguir o procedimento de localização de pacote sugerido [em Localizando um Windows do Instalador.](localizing-a-windows-installer-package.md)

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Atualize a documentação e Windows ferramentas de desenvolvimento do instalador do Windows.

-   As [Windows de](windows-installer-development-tools.md) Desenvolvimento do Instalador não são redistribuíveis e você só deve usar as versões dessas ferramentas disponíveis na Microsoft. Eles estão disponíveis nos componentes [do SDK do Windows](platform-sdk-components-for-windows-installer-developers.md) para desenvolvedores do Windows instalador no SDK (Software Development Kit) do Microsoft Windows.
-   Vários fornecedores de software independentes oferecem ferramentas para criar ou modificar Windows do Instalador. Essas ferramentas podem fornecer um ambiente de autor de pacote que pode ser mais fácil de usar do que as ferramentas fornecidas no SDK Windows Installer. Você pode saber mais sobre essas ferramentas nos recursos de informações discutidos em [Outras Fontes do Windows Informações do Instalador.](other-sources-of-windows-installer-information.md)
-   A capacidade de criar um pacote de arquivos de texto pode ser mais intuitiva para alguns desenvolvedores. O Windows de ferramentas xml do instalador (WiX) disponível Sourceforge.net [builds](https://sourceforge.net/projects/wix) Windows pacotes de instalação do código-fonte XML.
-   A documentação no [SDK Windows Instalador](./windows-installer-portal.md) do Windows lançada na Biblioteca Online do MSDN é atualizada com mais frequência.
-   Use a versão recente do [Msizap.exe](msizap-exe.md) (versão 3.1.4000.2726 ou superior) disponível nos Componentes do [SDK](platform-sdk-components-for-windows-installer-developers.md) do Windows para desenvolvedores do instalador do Windows para Windows Vista ou superior. Versões menores Msizap.exe podem remover informações sobre todas as atualizações que foram aplicadas a outros aplicativos no computador do usuário. Se essas informações são removidas, esses outros aplicativos talvez precisem ser removidos e reinstalados para receber atualizações adicionais.
-   O editor de tabela de [bancoOrca.exe](orca-exe.md) é um editor de tabela de banco de dados para criar e editar Windows de instalação e módulos de mesclagem. Ele tem uma interface gui básica, mas dá suporte à edição avançada de Windows do Instalador. Mesmo se você usar outro aplicativo como sua principal ferramenta de desenvolvimento, você poderá achar que usar Orca.exe é conveniente ao solucionar problemas e testar um pacote.
-   Consulte [Outras fontes](other-sources-of-windows-installer-information.md) de Windows informações do instalador do Windows atuais disponíveis em blogs, chats técnicos, grupos de notícias, artigos técnicos e sites.

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Se você decidir reempacodar um aplicativo de instalação herdado, siga as boas práticas de reempacodagem.

Muitos fornecedores de aplicativos fornecem pacotes Windows instalador nativos para a instalação ou seus produtos. Software que converte um aplicativo de instalação herdado existente em um Windows instalador é conhecido como uma ferramenta de reempaco. O whitepaper Guia passo a passo para criar pacotes do instalador do Windows e reempacodar software para o instalador [do Windows](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) descreve uma ferramenta de reempacolamento disponível comercialmente. O reempacodamento de um aplicativo de instalação existente não é a melhor prática de desenvolvimento. Os aplicativos que foram projetados desde o início para aproveitar os recursos Windows instalador podem ser mais fáceis para os usuários instalarem e service. Se você decidir usar um software de reempacodamento, as práticas a seguir poderão ajudá-lo a produzir um pacote Windows Instalador.

-   As ferramentas de reempacodagem convertem instalações herdadas em um pacote Windows Instalador do Windows tirar uma foto de um sistema de preparação antes e após a instalação. Todas as alterações de registro, alterações de arquivo ou configuração do sistema que ocorre durante o processo de captura são incluídas na instalação. Configure o hardware e o software do computador usado para reempacodar a instalação o mais próximo possível do sistema do usuário pretendido. Crie um pacote separado para cada configuração de hardware diferente. Reempacote usando um computador de preparação limpo. Remova todos os aplicativos desnecessários. Pare todos os processos desnecessários. Feche todos os serviços do sistema não essenciais.
-   Sempre faça uma cópia da instalação original antes de começar a trabalhar nele. Sempre trabalhe na cópia. Nunca pare um repacote antes de concluir a criação do pacote. Se o repacote danificar o pacote, você ainda terá o original.
-   Não reempacote as atualizações de software da Microsoft em um Windows instalador. A Microsoft lança atualizações de software, como service packs, como arquivos de extração automática que executam a instalação automaticamente. Essas atualizações usam instaladores diferentes do instalador Windows para substituir recursos Windows protegidos e não podem ser convertidas em um pacote Windows Instalador. Para obter informações sobre como implantar Windows service packs, consulte o guia de implantação do service pack no [Microsoft TechNet.](https://technet.microsoft.com/)
-   Não use uma ferramenta de reempacodamento para converter um Windows instalador em um novo pacote. O Windows instalador adiciona informações de configuração ao sistema, bem como aos recursos do aplicativo. Quando uma ferramenta de reempacotação compara o sistema antes e depois da instalação, o repacote interpreta indeminformamente as informações de configuração como parte do aplicativo. Isso geralmente causa danos ao aplicativo reempacodado. Em vez [disso, use as](a-customization-transform-example.md) transformação de personalização para modificar um pacote Windows instalador existente ou fazer um novo pacote. Você pode criar transformação de personalização usando a [Msitran.exe](msitran-exe.md) de personalização.
-   Não use uma ferramenta de reempacodamento para consolidar vários Windows do Instalador em um único pacote. Em vez disso, você [ pode usar aMsistuff.exe](msistuff-exe.md) para configurar o executável Setup.exe inicialização para instalar os pacotes um após o outro.
-   Faça seu Windows do instalador para que ele possa ser facilmente personalizado pelo cliente. As variáveis globais usadas pelo Windows instalador durante uma instalação podem ser definidas usando propriedades [públicas](properties.md) ou [transformações de personalização](a-customization-transform-example.md). Forneça documentação para o uso dessas propriedades e valores padrão práticos para todos os valores personalizáveis. Para obter informações sobre como obter e definir propriedades, consulte [Usando propriedades](using-properties.md). Para ver um exemplo de uma transformação de personalização, consulte Exemplo de transformação [de personalização](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>Não tente substituir recursos protegidos.

Windows Os pacotes do instalador não devem tentar substituir recursos protegidos durante a instalação ou atualização. O Windows instalador não remove nem substitui esses recursos porque Windows impede a substituição de arquivos essenciais do sistema, pastas e chaves do Registro. Proteger esses recursos impede falhas do aplicativo e do sistema operacional.

-   Ao executar no Windows Server 2008 ou no Windows Vista, o instalador do Windows ignora a instalação de qualquer arquivo ou chave do Registro protegida pela WRP (Proteção de Recursos do [Windows),](../wfp/windows-resource-protection-portal.md) o instalador inspeções um aviso no arquivo de log e continua com o restante da instalação sem um erro. Para obter informações, consulte [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).
-   WRP é o novo nome para a proteção Windows arquivo (WFP). A WRP protege chaves e pastas do Registro, bem como arquivos essenciais do sistema. No Windows Server 2003, Windows XP e Windows 2000, quando o instalador do Windows encontrou um arquivo protegido por WFP, o instalador solicitaria que o WFP instalasse o arquivo. Para obter informações, consulte [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>Não dependa de recursos não críticos.

Sua instalação ou atualização não deve depender da instalação de recursos não críticos pelos seguintes motivos.

-   As ações personalizadas poderão falhar se dependerem de um componente pertencente a um recurso que o usuário anuncia em vez de instalar.
-   As ações personalizadas sequenciadas antes [da ação InstallFinalize](installfinalize-action.md) poderão falhar se dependerem de um componente que contém um assembly que está sendo instalado. O Windows instalador não confirma assemblies no GAC (Cache de Assembly Global) até que a ação InstallFinalize seja concluída.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Use a API para recuperar informações Windows configuração do Instalador.

A instalação do seu aplicativo ou atualização não deve depender do acesso direto Windows informações de configuração do instalador salvas em seu computador. Em vez disso, use Windows interface de programação de aplicativos do instalador para recuperar informações de configuração. O local e o formato das informações de configuração são gerenciados pelo Windows instalador e podem ser alterados.

-   As funções de instalação e configuração da API Windows do instalador são descritas na [Referência de função do instalador.](installer-function-reference.md)
-   As [Propriedades de Configuração](property-reference.md) são descritas na Referência de Propriedade.
-   Os métodos e propriedades de automação são descritos na Referência [da Interface de Automação](automation-interface-reference.md). O script de WiLstPrd.vbs se conecta a um objeto Instalador e enumera produtos registrados e informações do produto. Para obter informações, [consulte Listar produtos, propriedades, recursos e componentes](list-products-properties-features-and-components.md).

## <a name="organize-the-installation-of-your-application-around-components"></a>Organize a instalação do aplicativo em torno dos componentes.

O Windows instalador do Windows instala ou remove coleções de recursos chamados de [componentes](windows-installer-components.md). Como os componentes normalmente são compartilhados, o autor de um pacote de instalação deve seguir as regras ao especificar os componentes de um recurso ou aplicativo.

-   Adera às [](organizing-applications-into-components.md) regras de componente ao organizar aplicativos em componentes para garantir que novos componentes, ou novas versões de componentes, possam ser instalados e removidos sem prejudicar outros aplicativos. Você pode seguir o procedimento descrito em [Definindo componentes do instalador](defining-installer-components.md).
-   O instalador rastreia todos os componentes pelo respectivo GUID de ID de componente especificado na [tabela Componente](component-table.md). É essencial para a operação do mecanismo de contagem de referência Windows Instalador do Windows que o GUID de ID do componente está correto. Siga as diretrizes em [Alterando o código do componente.](changing-the-component-code.md)
-   Se o pacote precisa quebrar as regras do componente, esteja ciente das possíveis consequências e certifique-se de que sua instalação nunca instale esses componentes em que eles possam danificar os componentes no sistema do usuário. Para obter informações, [consulte O que acontece se as regras de componente são interrompidas?](what-happens-if-the-component-rules-are-broken.md).
-   Esteja ciente de como o instalador Windows aplica as regras de [versão do arquivo](file-versioning-rules.md) ao substituir arquivos [existentes.](replacing-existing-files.md) O Windows instalador primeiro determina se o arquivo de chave do componente já está instalado antes de tentar instalar qualquer um dos arquivos do componente. Se o instalador encontrar um arquivo com o mesmo nome do arquivo de chave do componente instalado no local de destino, ele comparará a versão, a data e o idioma dos dois arquivos de chave e usará regras de versão do arquivo para determinar se o componente fornecido pelo pacote deve ser instalado. Se o instalador determinar que ele precisa substituir a base do componente no arquivo de chave, ele usará as regras de versão do arquivo em cada arquivo instalado para determinar se o arquivo deve ser substituído.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Reduza o tamanho de pacotes Windows instalador.

Pacotes de Windows muito grandes levam recursos do sistema e podem ser difíceis para os usuários instalarem. É uma boa prática reduzir o tamanho de pacotes Windows instalador muito grandes pelos métodos a seguir.

-   Compactar os arquivos na instalação e armazená-los em um arquivo de gabinete (.cab). O Instalador permite que o .cab seja armazenado como um arquivo externo separado ou como um fluxo de dados no próprio pacote MSI. Para obter informações, [consulte Usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).
-   Remova o espaço de armazenamento perdido no arquivo .msi usando uma das opções discutidas em [Reduzindo](reducing-the-size-of-an--msi-file.md)o tamanho de um arquivo .msi .
-   Se o Windows do instalador do banco de dados contiver mais de 32767 arquivos, você deverá alterar o esquema do banco de dados. Para obter [informações, consulte Authoring a Large Package](authoring-a-large-package.md).

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Se você usar ações personalizadas, siga as boas práticas de ação personalizadas.

O Windows instalador tem muitas ações [padrão](standard-actions-reference.md) integradas para a instalação e manutenção de aplicativos. Os desenvolvedores devem tentar contar com as ações padrão tanto quanto práticas, em vez de criar suas [próprias ações personalizadas.](custom-actions.md) No entanto, há situações em que o desenvolvedor de um pacote de instalação considera necessário escrever uma ação personalizada.

-   Siga as diretrizes para usar [ações personalizadas.](using-custom-actions.md)
-   Siga as [diretrizes para proteger ações personalizadas.](guidelines-for-securing-custom-actions.md) Ações personalizadas que usam informações confidenciais não devem gravar essas informações no log. Para obter informações, [consulte Segurança de ação personalizada.](custom-action-security.md)
-   As Ações Personalizadas não devem tentar definir um ponto Restauração do Sistema entrada de dentro de uma ação personalizada. Para obter informações, [consulte Configurando um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).
-   Retornar mensagens de erro de ações personalizadas e grave-as no log para facilitar a solução de problemas de ações personalizadas. Para obter informações, [consulte Ações personalizadas de mensagem de erro](error-message-custom-actions.md) e [Retornando mensagens de erro de ações personalizadas.](returning-error-messages-from-custom-actions.md)
-   Não altere o estado do sistema de uma ação personalizada imediata. Ações personalizadas que alteram o sistema diretamente ou chamam outro serviço do sistema devem ser adiadas para o momento em que o script de instalação é executado. Cada [ação personalizada de execução](deferred-execution-custom-actions.md) adiada que altera o estado do sistema deve ser precedida por uma ação personalizada de reação para desfazer a alteração de estado do sistema em uma re rollback de instalação. [](rollback-custom-actions.md) Para obter informações, [consulte Alterando o estado do sistema usando uma ação personalizada](changing-the-system-state-using-a-custom-action.md).
-   Ações personalizadas que executam operações de instalação complexas devem ser um [arquivo executável ou](executable-files.md) [uma biblioteca de vínculo dinâmico.](dynamic-link-libraries.md) Limite o uso de ações personalizadas com base em [scripts a](scripts.md) operações de instalação simples.
-   Faça com que os detalhes do que sua ação personalizada faça com o sistema facilmente descubram para os administradores do sistema. Coloque os detalhes de entradas e arquivos do Registro usados por sua ação personalizada em uma tabela personalizada e leia a ação personalizada desta tabela. Isso é demonstrado pelo exemplo em Usando uma ação [personalizada para criar contas de usuário em um computador local.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md) Para obter informações sobre como adicionar tabelas personalizadas a um banco de dados, consulte [Trabalhando](working-with-queries.md) com consultas e [exemplos](examples-of-database-queries-using-sql-and-script.md)de consultas de banco de dados usando SQL script e .
-   Uma ação personalizada não deve exibir uma caixa de diálogo. Ações personalizadas que exigem uma interface do usuário podem usar a [**função MsiProcessMessage.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) Consulte [Enviando mensagens para Windows instalador usando MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).
-   As ações personalizadas não devem usar nenhuma das funções listadas na página: Funções não [para uso em ações personalizadas.](functions-not-for-use-in-custom-actions.md)
-   Se a instalação for destinada a ser executado em um servidor terminal, teste se todas as suas ações personalizadas são capazes de ser executados em um servidor terminal. Para obter mais informações, [**consulte Propriedade TerminalServer.**](terminalserver.md)
-   Para executar uma ação personalizada quando um patch específico é desinstalado, a ação personalizada deve estar presente no aplicativo original ou estar em um patch para o produto que sempre é aplicado. Para obter mais informações, consulte [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).
-   As ações personalizadas não devem usar o nível da interface do usuário como uma condição para enviar mensagens de erro para o instalador porque isso pode interferir no registro em log e mensagens externas. Para obter informações, [consulte Determinando o nível da interface do usuário de uma ação personalizada.](determining-ui-level-from-a-custom-action.md)
-   Use instruções condicionais e Sintaxe de instrução condicional para garantir que seu pacote execute corretamente ações personalizadas, não execute ações personalizadas ou execute uma ação personalizada alternativa quando o pacote for desinstalado. [](conditional-statement-syntax.md) Teste se o pacote funciona conforme o esperado ao [desinstalar ações personalizadas.](uninstalling-custom-actions.md) Para obter informações, [consulte Ações de condicionação a executar durante a remoção](conditioning-actions-to-run-during-removal.md)
-   Se a instalação deve ser capaz de ser executado por usuários que não têm privilégios de administrador, teste para garantir que todas as ações personalizadas possam ser executados com privilégios não administradores. As ações personalizadas exigem privilégios elevados para modificar partes do sistema que não são específicas do usuário. O instalador poderá executar ações personalizadas com privilégios elevados se um aplicativo gerenciado estiver sendo instalado ou se a política do sistema tiver sido especificada para privilégios elevados. As ações personalizadas que exigem privilégios elevados devem incluir o msidbCustomActionTypeInScript e msidbCustomActionTypeNoImpersonate [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md) no tipo de ação personalizada. Isso é demonstrado pelo exemplo em Usando uma ação [personalizada para criar contas de usuário em um computador local.](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Se você usar assemblies, siga as boas práticas de assembly

Se o pacote usar [assemblies de](assemblies.md)software , siga as diretrizes para Adicionar [assemblies a](adding-assemblies-to-a-package.md)um pacote, Atualizando [assemblies](updating-assemblies.md)e Instalando e [removendo assemblies](installing-and-removing-assemblies.md).

## <a name="do-not-ship-concurrent-installations"></a>Não enviar instalações simultâneas.

[Instalações simultâneas ,](concurrent-installations.md)também chamadas de Instalações Aninhadas, instale outro Windows instalador durante uma instalação em execução no momento. O uso de instalações simultâneas não é uma boa prática porque são difíceis para os clientes atenderem. A a patch e a atualização podem não funcionar com instalações simultâneas. a alternativa recomendada ao uso de instalações simultâneas é usar um aplicativo de instalação e um manipulador de interface de usuário externo para instalar vários pacotes de Windows Installer em sequência.

Para obter mais informações sobre como usar um manipulador de interface do usuário externo, consulte [monitorando uma instalação usando o MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md). Para obter mais informações sobre como usar um manipulador externo baseado em registro, consulte [monitorando uma instalação usando o MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

As instalações simultâneas, às vezes, são usadas em ambientes corporativos controlados para instalar aplicativos que não são destinados ao público. Siga estas diretrizes se você decidir usar instalações simultâneas.

-   Não use instalações simultâneas para instalar ou atualizar um produto de remessa.
-   Instalações simultâneas não devem compartilhar componentes.
-   Uma instalação administrativa não deve conter uma instalação simultânea.
-   As ProgressBars integradas não devem ser usadas com instalações simultâneas.
-   Os recursos que devem ser anunciados não devem ser instalados por uma instalação simultânea.
-   Um pacote que executa uma instalação simultânea de um aplicativo também deve desinstalar o aplicativo simultâneo quando o produto pai é desinstalado. Existe uma instalação aninhada no contexto do produto pai em Adicionar ou remover programas no painel de controle.

## <a name="keep-package-names-and-package-codes-consistent"></a>Mantenha os nomes de pacote e os códigos de pacote consistentes.

O arquivo de .msi pode receber qualquer nome que ajude os usuários a identificar o pacote, mas o nome não deve ser alterado sem alterar também o código do produto.

-   dê ao seu arquivo de .msi um nome amigável que permita ao usuário identificar o conteúdo do pacote de Windows Installer.
-   O [código do produto](product-codes.md) é a identificação principal de um aplicativo e deve ser alterado sempre que houver uma atualização abrangente para o aplicativo. Para obter informações, consulte [**ProductCode**](productcode.md) e [alterando o código do produto](changing-the-product-code.md). Alterar o nome do arquivo de .msi do aplicativo é considerado uma alteração abrangente e sempre requer uma alteração correspondente do código do produto para manter a consistência.
-   O [código do pacote](package-codes.md) é o identificador principal usado pelo instalador para pesquisar e validar o pacote correto para uma determinada instalação. Dois arquivos de .msi não idênticos já devem ter o mesmo código de pacote. Se um pacote for alterado sem alterar o código do pacote, o instalador não poderá usar o pacote mais recente se ambos ainda estiverem acessíveis ao instalador. O código do pacote é armazenado na propriedade [**Resumo do número de revisão**](revision-number-summary.md) do fluxo de informações de [Resumo](summary-information-stream.md).
-   Observe que as letras no código do produto e nos [GUIDs](guid.md) de código do pacote devem ser maiúsculas.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>Não use as tabelas SelfReg e TypeLib.

-   Os autores do pacote de instalação são altamente aconselhados em relação ao uso do auto-registro e da tabela [selfreg](selfreg-table.md) . Em vez disso, eles devem registrar módulos criando uma ou mais das tabelas no [grupo tabelas do registro](registry-tables-group.md). muitos dos benefícios da Windows Installer são perdidos com o auto-registro porque as rotinas de autoregistro tendem a ocultar informações de configuração críticas. Para obter uma lista dos motivos para evitar o auto-registro, consulte a [tabela selfreg](selfreg-table.md).
-   Os autores do pacote de instalação são altamente aconselhados em relação ao uso da tabela [TypeLib](typelib-table.md) . Em vez de usar a tabela TypeLib, registre bibliotecas de tipos usando a tabela [do registro](registry-table.md) . Se uma instalação que usa a tabela TypeLib falhar e precisar ser revertida, a reversão poderá não restaurar o computador para o mesmo estado que existia antes da reversão.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Forneça a opção para instalar sem uma interface do usuário.

Os administradores geralmente preferem implantar aplicativos dentro de uma empresa sem exigir interação do usuário. É uma boa prática habilitar seu aplicativo para fornecer a opção de ser instalada com o [nível de interface do usuário](user-interface-levels.md) de nenhum.

-   Use [Propriedades públicas](public-properties.md) para obter informações de configuração. Os administradores podem fornecer essas informações na linha de comando.
-   Não exija que a instalação dependa das informações coletadas da interação do usuário com caixas de diálogo. Essas informações não estão disponíveis durante uma instalação silenciosa.
-   Não reinicie automaticamente o computador do usuário durante uma instalação silenciosa.
-   Os administradores podem definir o [nível de interface do usuário](user-interface-levels.md) ao instalar o usando a opção de linha de [comando](command-line-options.md) "/q". O nível da interface do usuário também pode ser definido programaticamente com uma chamada para [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Evite usar a política AlwaysInstallElevated.

Se a política [AlwaysInstallElevated](alwaysinstallelevated.md) não estiver definida, os aplicativos não distribuídos pelo administrador serão instalados usando os privilégios do usuário e somente os aplicativos gerenciados terão privilégios elevados. definir essa política direciona Windows Installer para usar permissões do sistema ao instalar o aplicativo no sistema. Esse método pode abrir um computador para um risco de segurança, porque quando essa política é definida, um usuário não administrador pode executar instalações com privilégios [*elevados*](e-gly.md) e acessar locais seguros no computador. É uma boa prática usar outro método do que a política de AlwaysInstallElevated ao [instalar um pacote com privilégios elevados para um não administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md) ou [aplicação de patches Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Habilite a política DisableMedia para limitar a instalação não autorizada.

A política [DisableMedia](disablemedia.md) pode impedir a instalação não autorizada de aplicativos. Quando essa política está habilitada, os usuários e administradores que executam uma instalação de manutenção de um produto são impedidos de usar a caixa de diálogo de procura para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis. Procurar outros produtos é impedido, independentemente de a instalação ser feita com privilégios elevados. Ainda é possível que o usuário reinstale o produto da mídia se o usuário tiver uma origem de mídia rotulada corretamente.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Mantenha os arquivos de origem do pacote original seguros e disponíveis para os usuários.

em alguns casos, a origem original do pacote de Windows Installer pode ser necessária para instalar-sob demanda, reparar ou atualizar um aplicativo. Se o instalador não conseguir localizar uma fonte disponível, será solicitado que o usuário forneça a mídia ou vá para um local de rede que contenha as fontes necessárias. É uma boa prática garantir que o instalador tenha as fontes necessárias sem precisar solicitar o usuário.

-   Use [assinaturas digitais e arquivos de gabinete externo](digital-signatures-and-external-cabinet-files.md) para garantir que as origens de origem usadas pelo instalador sejam seguras. Uma imagem de origem não compactada armazenada em um local público não é segura.
-   Inclua uma lista completa de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo na propriedade [**SourceList**](sourcelist.md) .
-   Use um compartilhamento de Sistema de Arquivos Distribuído (DFS) para o caminho de origem.
-   Use a API Windows Installer para recuperar e modificar informações de lista de origem para aplicativos e patches de Windows Installer. Para obter informações, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).
-   Use os métodos e as propriedades do [**objeto do instalador**](installer-object.md), [**objeto de produto**](product-object.md)e [**objeto de Patch**](patch-object.md) para recuperar e modificar informações de lista de origem para aplicativos Windows Installer e patches.
-   Siga os pontos listados em [impedindo que um patch requeira acesso aos pontos de origem de instalação originais](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) para minimizar a possibilidade de o patch precisar de acesso às fontes originais.
-   Armazene os arquivos de origem do pacote em um local que não seja a pasta temporária do sistema. Windows Os arquivos de origem do instalador armazenados na pasta temporária podem ficar indisponíveis para os usuários.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Habilite o log detalhado no computador do usuário ao solucionar problemas de implantação.

[Windows Installer log](windows-installer-logging.md) inclui uma opção de log detalhado que pode ser habilitada no computador de um usuário. as informações em um log detalhado podem ser úteis ao tentar solucionar problemas de implantação de pacote Windows Installer.

-   Você pode habilitar o log detalhado no computador do usuário usando [Opções de linha de comando](command-line-options.md), a propriedade [**MsiLogging**](msilogging.md) , a política de [registro em log](logging.md), o [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)e o método [**EnableLog**](installer-enablelog.md) .
-   um recurso muito útil para interpretar Windows Installer arquivos de log é [Wilogutl.exe](wilogutl-exe.md). Essa ferramenta ajuda a análise de arquivos de log e exibe soluções sugeridas para erros encontrados em um arquivo de log.
-   para obter mais informações sobre como interpretar Windows Installer arquivos de log, consulte a white paper disponível no site do TechNet: [Windows Installer: benefícios e implementação para administradores do sistema](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   A opção de log detalhado deve ser usada somente para fins de solução de problemas e não deve ser deixada porque pode ter efeitos adversos no desempenho do sistema e no espaço em disco. Cada vez que você usa a ferramenta Adicionar/remover programas no painel de controle, um novo arquivo é criado.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>A desinstalação deixa o computador do usuário em um estado limpo.

A remoção do aplicativo é tão importante quanto a instalação. quando um pacote de Windows Installer é desinstalado, ele não deve deixar nenhuma parte inútil dele atrás no computador do usuário.

-   Se um arquivo que deveria ter sido removido do computador do usuário permanecer instalado após a execução de uma desinstalação, talvez o instalador não esteja removendo o componente que contém o arquivo por um ou mais dos motivos descritos em [removendo arquivos perdidos](removing-stranded-files.md).
-   Se um aplicativo precisar ser registrado, crie o pacote para remover informações do registro quando o aplicativo for desinstalado. Para obter informações, consulte [adicionando ou removendo chaves do registro na instalação ou remoção de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). se um aplicativo não estiver registrado, o aplicativo não estará listado no recurso adicionar ou remover programas no painel de controle e não poderá ser gerenciado usando o Windows Installer.
-   para ocultar um aplicativo do recurso adicionar ou remover programas no painel de controle e ainda poder usar o Windows Installer para gerenciar o aplicativo, siga as diretrizes descritas em [adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).
-   As ações personalizadas devem ser condicionadas para serem executadas ou não, conforme necessário, após a desinstalação. Diferentes ações personalizadas talvez precisem ser executadas na instalação e na desinstalação.
-   As informações de personalização específicas do usuário podem ser armazenadas em um arquivo de texto no computador. Isso tem a vantagem de que o arquivo pode ser removido quando o aplicativo é desinstalado, mesmo que o usuário dessa personalização não esteja conectado no momento.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Pacotes de teste para a implantação de instalação por usuário e por computador.

É uma boa prática permitir que os clientes decidam se deseja implantar um pacote para instalação no [contexto de instalação](installation-context.md)por computador ou por usuário.

-   Considere se o aplicativo deve estar disponível somente para usuários específicos ou para todos os usuários do computador durante o processo de desenvolvimento.
-   Teste se o pacote funciona corretamente para a instalação por usuário e contextos de instalação por máquina.
-   Torne o pacote facilmente personalizável e permita que os clientes decidam se desejam implantá-los por usuário ou por computador.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Planeje e teste uma estratégia de serviço antes de enviar o aplicativo.

Você deve decidir como pretende atender o aplicativo antes de implantar o aplicativo pela primeira vez.

-   Considere os tipos de atualizações que você pretende usar para atender seu aplicativo no futuro. o Windows Installer fornece três tipos de atualizações: [atualização pequena](small-updates.md), [atualização secundária](minor-upgrades.md)e [atualizações principais](major-upgrades.md). As diferenças entre eles são descritas no tópico [patches e atualizações](patching-and-upgrades.md) .
-   Antes de enviar seu aplicativo, teste se ele funciona conforme o esperado após a manutenção com cada tipo de atualização.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Reduza a dependência de atualizações nas fontes originais.

Se os arquivos de origem originais forem necessários para atualizar seu aplicativo, isso poderá dificultar a manutenção do aplicativo. Os métodos a seguir podem ajudar a reduzir a dependência de atualizações nas fontes originais.

-   Use um [*patch Delta*](d-gly.md) para atualizar as versões de linha de base do seu aplicativo, como a versão RTM e as versões de Service Pack. Siga as diretrizes para usar os patches Delta descritos no tópico: [reduzindo o tamanho do patch](reducing-patch-size.md).
-   Siga as recomendações listadas no tópico: [impedir que um patch exija acesso à fonte de instalação original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>Não distribua módulos de mesclagem sem serviço.

Os aplicativos não devem depender de [módulos de mesclagem](merge-modules.md) para a instalação do componente se o proprietário do módulo de mesclagem e o proprietário do aplicativo forem diferentes. Isso pode dificultar o serviço do aplicativo porque ambos os proprietários precisam coordenar para atualizar o aplicativo ou o módulo. Sem conhecer todos os aplicativos que usaram o módulo de mesclagem, o proprietário do aplicativo não é capaz de atualizar o módulo de mesclagem sem arriscar que a atualização possa ser incompatível com outro aplicativo. o proprietário do módulo de mesclagem não tem nenhum método direto para atualizar Windows Installer pacotes que já instalaram o módulo de mesclagem.

-   considere fornecer os componentes necessários aos usuários como outro Windows Installer instalação.

## <a name="avoid-patching-administrative-installations"></a>Evite aplicar patches em instalações administrativas.

forneça em uma rede uma [instalação administrativa](administrative-installation.md) do pacote de Windows Installer original do seu aplicativo para permitir que os membros de um grupo de trabalho instalem o aplicativo. Os usuários dessa imagem administrativa devem aplicar atualizações à instância local do aplicativo localizado em seu computador. Isso mantém os usuários em sincronia com a imagem administrativa. Não é recomendável aplicar atualizações à instalação administrativa pelos seguintes motivos.

-   O tamanho e a latência do download necessários para que os usuários obtenham uma atualização são aumentados em comparação com o download de um patch. todo o pacote de Windows Installer e arquivos de origem atualizados devem ser baixados, rearmazenados em cache e reinstalados.
-   Os usuários não podem fazer a [instalação sob demanda](installation-on-demand.md) e reparar aplicativos de uma instalação administrativa atualizada até que eles rearmazenem novamente em cache e reinstalem o aplicativo.
-   A aplicação de um patch a uma instalação administrativa remove a assinatura digital do pacote. Um administrador deve desistir do pacote. para obter mais informações sobre como usar assinaturas digitais, consulte [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).
-   Muitos patches binários visam a imagem RTM do aplicativo e exigem uma versão de arquivo anterior. A instância local de um aplicativo instalado de uma instalação administrativa atualizada pode não funcionar com outras atualizações. Muitos aplicativos de patch binários podem falhar.
-   A aplicação de um patch a uma instalação administrativa atualiza os arquivos de origem e o arquivo de .msi, mas não carimba a imagem de rede com informações sobre a atualização. Os usuários não podem determinar quais atualizações foram recebidas da instalação administrativa. Isso torna impossível sequenciar as atualizações aplicadas no lado do usuário com aquelas já aplicadas no lado da imagem administrativa.
-   Os patches aplicados a uma instalação administrativa não são [patches desinstaláveis](uninstallable-patches.md). Isso pode impedir que o código do pacote em cache no computador do usuário se torne diferente do código do pacote na instalação administrativa. Se o código do pacote armazenado em cache no computador do usuário se tornar diferente daquele na instalação administrativa, reinstale o aplicativo da instalação administrativa e, em seguida, corrija o computador cliente.
-   Se você decidir aplicar pequenas atualizações por meio da aplicação de patch em uma imagem administrativa, siga as diretrizes descritas no tópico: [aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md).

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registre as atualizações para executar com privilégios elevados.

a partir do Windows Installer 3,0, é possível aplicar patches a um aplicativo que foi instalado em um contexto gerenciado por usuário, depois que o patch tiver sido registrado como tendo privilégios elevados. você não pode aplicar patches a aplicativos que estão instalados em um contexto gerenciado por usuário usando versões do Windows Installer anteriores à versão 3,0.

-   Use o método [**SourceListAddSource**](patch-sourcelistaddsource.md) ou a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar um pacote de patch como tendo privilégios elevados. Siga as diretrizes e os exemplos fornecidos na [aplicação de patches Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).
-   ao executar Windows Installer versão 4,0 no Windows Vista, você também pode usar a [aplicação de patches de controle de conta de usuário (UAC)](user-account-control--uac--patching.md) para permitir que os autores de instalações de Windows Installer identifiquem patches assinados digitalmente que podem ser aplicados no futuro por usuários não administradores. Isso só está disponível com a instalação de pacotes no [contexto de instalação](installation-context.md) por máquina (AllUsers = 1).
-   Verifique se a aplicação de patches com privilégios mínimos não foi desabilitada definindo a propriedade [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) ou a política [DisableLUAPatching](disableluapatching.md) .

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Use a tabela MsiPatchSequence para sequenciar patches.

Inclua uma [tabela MsiPatchSequence](msipatchsequence-table.md) em seu pacote e adicione informações de sequenciamento de patch. a partir do Windows Installer versão 3,0, o instalador pode usar a tabela MsiPatchSequence ao [instalar vários patches](installing-multiple-patches.md) para determinar a melhor sequência de aplicativos de patch. Use as diretrizes descritas no [sequenciamento de patches no Windows Installer versão 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) white paper para definir as famílias de patches.

-   Se for prático, especifique todos os patches como pertencentes a uma única família de patches. Em muitos casos, uma única família de patches fornece flexibilidade suficiente para os patches de sequência. A complexidade da criação aumenta quando várias famílias de patches são usadas. Atribua um nome significativo à família de patches e atribua valores de sequência na família de patches que aumentam ao longo do tempo. Siga o [exemplo de várias correções](multiple-patching-example.md) para aplicar patches na ordem em que foram emitidos.
-   Use a [tabela PatchSequence](patchsequence-table--patchwiz-dll-.md) em [Patchwiz.dll](patchwiz-dll.md) para gerar as informações na [tabela MsiPatchSequence](msipatchsequence-table.md). a versão do PATCHWIZ.DLL lançada com Windows Installer 3,0 pode gerar automaticamente informações de sequenciamento de patch. Para obter mais informações sobre como adicionar um novo patch, consulte [gerando informações de sequência de patch](generating-patch-sequence-information---patchwiz-dll-.md). para obter mais informações sobre cenários de sequenciamento de patch, consulte o white paper: [sequenciamento de patch no Windows Installer versão 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3).

## <a name="test-the-installation-package-thoroughly"></a>Teste o pacote de instalação completamente.

teste a instalação, o reparo e a remoção corretas do pacote de Windows Installer. Você pode dividir seu processo de teste nas seguintes partes.

-   Teste de instalação – teste a instalação com todas as combinações possíveis de recursos de aplicativo. Testar todos os tipos de instalação, incluindo a [instalação administrativa](administrative-installation.md), a [reversão da instalação](rollback-installation.md)e [a instalação sob demanda](installation-on-demand.md). Experimente todos os possíveis métodos de instalação, incluindo clicar no arquivo de .msi, [Opções de linha de comando](command-line-options.md)e instalar no painel de controle. Teste se o pacote pode ser instalado por usuários em todos os possíveis contextos de privilégio. Tente instalar o pacote depois que ele tiver sido implantado por todos os métodos possíveis. habilite o [log de Windows Installer](windows-installer-logging.md) para cada teste e resolva todos os erros encontrados no log do instalador e no log de eventos.
-   Teste de interface do usuário-teste o pacote quando instalado com todos os [níveis de interface do usuário](user-interface-levels.md)possíveis. Teste o pacote instalado sem interface do usuário e com todas as informações fornecidas por meio da interface do usuário. Verifique a [acessibilidade](accessibility.md) da interface do usuário e se a interface do usuário funciona como esperado para diferentes resoluções de tela e tamanhos de fonte.
-   Manutenção e reparo de teste – teste se o pacote pode lidar com [patches e atualizações](patching-and-upgrades.md) entregues por uma [pequena atualização](small-updates.md), [atualização secundária](minor-upgrades.md)e [atualizações importantes](major-upgrades.md). Antes de implantar o pacote, grave uma atualização de avaliação de cada tipo e tente aplicá-lo ao pacote original.
-   Teste de desinstalação – Verifique se quando o pacote é removido ele não deixa nenhuma parte inútil de si mesmo no computador do usuário e se apenas as informações pertencentes ao pacote foram removidas. Reinicialize o computador de teste após desinstalar o pacote e verificar a integridade das ferramentas de sistema comuns e outros aplicativos padrão. Teste se o pacote pode ser removido por usuários em todos os possíveis contextos de privilégio. Teste todos os métodos para remover o pacote, clique no arquivo .msi, tente as [Opções de linha de comando](command-line-options.md)e tente remover o pacote do painel de controle. habilite o [log de Windows Installer](windows-installer-logging.md) para cada teste e resolva todos os erros encontrados no log do instalador e no log de eventos.
-   Teste de funcionalidade do produto – Verifique se o aplicativo funciona conforme o esperado após a instalação, o reparo ou a remoção do pacote.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Corrija todos os erros de validação antes de implantar um pacote de instalação novo ou revisado.

execute a [validação de pacote](package-validation.md) em um pacote de Windows Installer novo ou revisado antes de tentar instalá-lo pela primeira vez. a validação verifica se há erros na criação do banco de dados Windows Installer. A tentativa de instalar um pacote que não passe na validação pode danificar o sistema do usuário.

-   Você pode validar seu pacote usando [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md). ambas as ferramentas são fornecidas com o SDK do Windows. Os fornecedores terceirizados também podem incorporar o sistema de validação ICE ao seu ambiente de criação.
-   Você pode usar o conjunto padrão de [avaliadores de consistência internos-ICES](internal-consistency-evaluators-ices.md) incluídos nos arquivos. Cub fornecidos com o SDK ou personalizar a validação [criando um Ice](building-an-ice.md) e adicionando-o ao arquivo. cub.
-   Você pode usar o Evalcom2.dll para implementar a [automação de validação](validation-automation.md) para pacotes de instalação e módulos de mesclagem.

## <a name="author-a-secure-installation"></a>Crie uma instalação segura.

Seguindo essas diretrizes ao desenvolver seu pacote para ajudar a manter um ambiente seguro durante a instalação.

-   [Diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md)
-   [Diretrizes para proteger pacotes em computadores bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md)
-   [Diretrizes para proteger ações personalizadas](guidelines-for-securing-custom-actions.md)

## <a name="use-pmsihandle-instead-of-handle"></a>Usar PMSIHANDLE em vez de identificador

As variáveis de tipo **PMSIHANDLE** são definidas em MSI. h. É recomendável que seu aplicativo use o tipo **PMSIHANDLE** porque o instalador fecha os objetos **PMSIHANDLE** à medida que eles saem do escopo, enquanto seu aplicativo deve fechar os objetos **MSIHANDLE** chamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).

Por exemplo, se você usar um código como este:

``` syntax
MSIHANDLE hRec = MsiCreateRecord(3);
```

Altere-o para:

``` syntax
PMSIHANDLE hRec = MsiCreateRecord(3);
```

 

 
