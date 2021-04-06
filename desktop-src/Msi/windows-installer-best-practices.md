---
description: 'Esta seção enumera uma lista de dicas, vinculadas à documentação principal do SDK do Windows Installer, para ajudar os desenvolvedores de aplicativos, os autores de instalação, os profissionais de ti e os desenvolvedores de infraestrutura a descobrir as práticas recomendadas para usar o Windows Installer:'
ms.assetid: ff48d995-fe6f-4d1b-898d-67574ed3c5b7
title: Práticas recomendadas de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffaf6aae83afbe510f2b1eefc447e34754296ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011291"
---
# <a name="windows-installer-best-practices"></a>Práticas recomendadas de Windows Installer

Esta seção enumera uma lista de dicas, vinculadas à documentação principal do SDK do Windows Installer, para ajudar os desenvolvedores de aplicativos, os autores de instalação, os profissionais de ti e os desenvolvedores de infraestrutura a descobrir as práticas recomendadas para usar o Windows Installer:

-   [Atualize a versão do Windows Installer.](#update-the-windows-installer-version)
-   [Atenda aos requisitos de certificação do logotipo do Windows.](#meet-the-windows-logo-certification-requirements)
-   [Prepare o pacote para localização.](#prepare-the-package-for-localization)
-   [Atualize suas ferramentas e documentação de desenvolvimento de Windows Installer.](#update-your-windows-installer-development-tools-and-documentation)
-   [Se você decidir reempacotar um aplicativo de instalação herdado, siga as boas práticas de reempacotamento.](#if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices)
-   [Não tente substituir os recursos protegidos.](#do-not-try-to-replace-protected-resources)
-   [Não dependa de recursos não críticos.](#do-not-depend-upon-non-critical-resources)
-   [Use a API para recuperar Windows Installer informações de configuração.](#use-the-api-to-retrieve-windows-installer-configuration-information)
-   [Organize a instalação do seu aplicativo com base em componentes.](#organize-the-installation-of-your-application-around-components)
-   [Reduza o tamanho de pacotes de Windows Installer grandes.](#reduce-the-size-of-large-windows-installer-packages)
-   [Se você usar ações personalizadas, siga as boas práticas de ação personalizadas.](#if-you-use-custom-actions-follow-good-custom-action-practices)
-   [Se você usar assemblies, siga as práticas de assembly adequadas](#if-you-use-assemblies-follow-good-assembly-practices)
-   [Não envie instalações simultâneas.](#do-not-ship-concurrent-installations)
-   [Mantenha os nomes de pacote e os códigos de pacote consistentes.](#keep-package-names-and-package-codes-consistent)
-   [Não use as tabelas SelfReg e TypeLib.](#do-not-use-the-selfreg-and-typelib-tables)
-   [Forneça a opção para instalar sem uma interface do usuário.](#provide-the-option-to-install-without-a-user-interface)
-   [Evite usar a política AlwaysInstallElevated.](#avoid-using-the-alwaysinstallelevated-policy)
-   [Habilite a política DisableMedia para limitar a instalação não autorizada.](#enable-the-disablemedia-policy-to-limit-unauthorized-installation)
-   [Mantenha os arquivos de origem do pacote original seguros e disponíveis para os usuários.](#keep-the-original-package-source-files-secure-and-available-to-users)
-   [Habilite o log detalhado no computador do usuário ao solucionar problemas de implantação.](#enable-verbose-logging-on-users-computer-when-troubleshooting-deployment)
-   [A desinstalação deixa o computador do usuário em um estado limpo.](#uninstallation-leaves-the-users-computer-in-a-clean-state)
-   [Pacotes de teste para a implantação de instalação por usuário e por computador.](#test-packages-for-both-per-user-and-per-machine-installation-deployment)
-   [Planeje e teste uma estratégia de serviço antes de enviar o aplicativo.](#plan-and-test-a-servicing-strategy-before-shipping-the-application)
-   [Reduza a dependência de atualizações nas fontes originais.](#reduce-the-dependency-of-updates-upon-the-original-sources)
-   [Não distribua módulos de mesclagem sem serviço.](#do-not-distribute-unserviceable-merge-modules)
-   [Evite aplicar patches em instalações administrativas.](#avoid-patching-administrative-installations)
-   [Registre as atualizações para executar com privilégios elevados.](#register-updates-to-run-with-elevated-privilege)
-   [Use a tabela MsiPatchSequence para sequenciar patches.](#use-the-msipatchsequence-table-to-sequence-patches)
-   [Teste o pacote de instalação completamente.](#test-the-installation-package-thoroughly)
-   [Corrija todos os erros de validação antes de implantar um pacote de instalação novo ou revisado.](#fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package)
-   [Crie uma instalação segura.](#author-a-secure-installation)
-   [Usar PMSIHANDLE em vez de identificador](#use-pmsihandle-instead-of-handle)

## <a name="update-the-windows-installer-version"></a>Atualize a versão do Windows Installer.

-   Use Windows Installer 5,0 no Windows Server 2008 R2 e no Windows 7. Essa é a versão Windows Installer fornecida com o sistema operacional.
-   Use Windows Installer 4,5 no Windows Server 2008, Windows Server 2003 com Service Pack 1 (SP1), Windows Vista com Service Pack 1 (SP1) ou Windows XP com Service Pack 2 (SP2). Para obter informações sobre como obter a versão mais recente do Windows Installer, consulte [Windows Installer redistribuíveis](windows-installer-redistributables.md).
-   Use Windows Installer 3,1 no Windows 2000 com Service Pack 3 (SP3). Windows Installer versão 3,1 tem recursos que facilitam o melhor serviço de aplicativos e aplicação de [patches](patching.md).
-   Muitos recursos importantes foram introduzidos com a versão 3,0 e estão listados na seção [sem suporte na versão 2,0 do Windows Installer](not-supported-in-windows-installer-version-2-0.md). Os pacotes de instalação e as atualizações que foram criadas para o Windows Installer 2,0 podem ser instalados usando o Windows Installer 3,0 e posterior. Os pacotes de patches que contêm as novas tabelas usadas pelo Windows Installer 3,0 ainda podem ser aplicados usando versões anteriores do Windows Installer, mas sem a funcionalidade de patches do Windows Installer 3,0. Também é possível criar patches que exigem explicitamente o Windows Installer 3,0 que não podem ser aplicados por versões anteriores do Windows Installer. Se um usuário não puder atualizar a versão do instalador, verifique se seu aplicativo ou atualização será compatível com uma atualização futura do Windows Installer.
-   Para obter uma lista dos recursos de Windows Installer sem suporte nas versões anteriores do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).

## <a name="meet-the-windows-logo-certification-requirements"></a>Atenda aos requisitos de certificação do logotipo do Windows.

-   Mesmo que você não pretenda enviar seu aplicativo para o programa de logotipo, seguindo as diretrizes de certificação de logotipo pode ajudar a melhorar o pacote de Windows Installer. Para obter uma visão geral dos requisitos de logotipo e links para programas de certificação de logotipo específicos, consulte [requisitos de Windows Installer e logotipo](windows-installer-and-logo-requirements.md).

## <a name="prepare-the-package-for-localization"></a>Prepare o pacote para localização.

-   É uma prática recomendada preparar-se para a localização futura ao criar o pacote de instalação original. Você pode seguir o procedimento de localização de pacote sugerido na [localização de um pacote de Windows Installer](localizing-a-windows-installer-package.md).

## <a name="update-your-windows-installer-development-tools-and-documentation"></a>Atualize suas ferramentas e documentação de desenvolvimento de Windows Installer.

-   As [ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md) não são redistribuíveis e você só deve usar as versões dessas ferramentas disponíveis na Microsoft. Eles estão disponíveis na [SDK do Windows componentes para Windows Installer desenvolvedores](platform-sdk-components-for-windows-installer-developers.md) no SDK (Software Development Kit) do Microsoft Windows.
-   Vários fornecedores independentes de software oferecem ferramentas para criar ou modificar pacotes de Windows Installer. Essas ferramentas podem fornecer um ambiente de criação de pacotes que pode ser mais fácil de usar do que as ferramentas fornecidas no SDK do Windows Installer. Você pode saber mais sobre essas ferramentas dos recursos de informações discutidos em [outras fontes de Windows Installer informações](other-sources-of-windows-installer-information.md).
-   A capacidade de criar um pacote a partir de arquivos de texto pode ser mais intuitiva para alguns desenvolvedores. O conjunto de ferramentas WiX (Windows Installer XML) disponível no [sourceforge.net](https://sourceforge.net/projects/wix) cria pacotes de instalação do Windows do código-fonte XML.
-   A documentação no [SDK do Windows Installer](./windows-installer-portal.md) lançado na biblioteca MSDN online é atualizada com mais frequência.
-   Use a versão recente do [Msizap.exe](msizap-exe.md) (versão 3.1.4000.2726 ou superior) que está disponível na [SDK do Windows componentes para Windows Installer desenvolvedores](platform-sdk-components-for-windows-installer-developers.md) para Windows Vista ou superior. Versões menores do Msizap.exe podem remover informações sobre todas as atualizações que foram aplicadas a outros aplicativos no computador do usuário. Se essas informações forem removidas, talvez esses outros aplicativos precisem ser removidos e reinstalados para receber atualizações adicionais.
-   O editor de tabela de banco de dados [Orca.exe](orca-exe.md) é um editor de tabela de banco de dados para criar e editar Windows Installer pacotes e Mesclar módulos. Ele tem uma interface de GUI básica, mas dá suporte à edição avançada de bancos de dados do Windows Installer. Mesmo que você use outro aplicativo como sua ferramenta de desenvolvimento principal, talvez você ache que usar Orca.exe é conveniente ao solucionar problemas e testar um pacote.
-   Consulte [outras fontes de Windows Installer informações](other-sources-of-windows-installer-information.md) para obter informações de Windows Installer atuais disponíveis em Blogs, bate-papos técnicos, grupos de notícias, artigos técnicos e sites.

## <a name="if-you-decide-to-repackage-a-legacy-setup-application-follow-good-repackaging-practices"></a>Se você decidir reempacotar um aplicativo de instalação herdado, siga as boas práticas de reempacotamento.

Muitos fornecedores de aplicativos fornecem pacotes Windows Installer nativos para a instalação ou seus produtos. O software que converte um aplicativo de instalação herdado existente em um pacote Windows Installer é conhecido como uma ferramenta de reempacotamento. O White Paper [guia passo a passo para a criação de pacotes de Windows Installer e o reempacotamento de software para a Windows Installer](https://www.microsoft.com/technet/prodtechnol/windows2000serv/howto/winstall.mspx) descreve uma ferramenta de reempacotamento comercialmente disponível. Reempacotar um aplicativo de instalação existente não é a melhor prática de desenvolvimento. Os aplicativos que foram projetados desde o início para aproveitar os recursos de Windows Installer podem ser mais fáceis de instalar e atender aos usuários. Se você decidir usar um software de reempacotamento, as práticas a seguir podem ajudá-lo a produzir um pacote de Windows Installer melhor.

-   As ferramentas de reempacotamento convertem instalações herdadas em um pacote Windows Installer tirando uma imagem de um sistema de preparo antes e depois da instalação. Qualquer alteração no registro, alteração de arquivo ou configuração do sistema que ocorre durante o processo de captura é incluída na instalação do. Configure o hardware e o software do computador usado para reempacotar a instalação o mais próximo possível do sistema do usuário pretendido. Crie um pacote separado para cada configuração de hardware diferente. Reempacotar usando um computador de preparo limpo. Remova todos os aplicativos desnecessários. Interrompa todos os processos desnecessários. Feche todos os serviços do sistema não essenciais.
-   Sempre faça uma cópia da instalação original antes de começar a trabalhar nela. Sempre trabalhe na cópia. Nunca interrompa um reempacotador antes de concluir a compilação do pacote. Se o reempacotador danificar o pacote, você ainda terá o original.
-   Não reempacote as atualizações de software da Microsoft em um pacote Windows Installer. A Microsoft lança atualizações de software, como Service Packs, como arquivos de extração automática que executam a instalação automaticamente. Essas atualizações usam instaladores diferentes do Windows Installer para substituir recursos protegidos do Windows e não podem ser convertidas em um pacote Windows Installer. Para obter informações sobre como implantar Service Packs do Windows, consulte o guia de implantação do service pack no [Microsoft TechNet](https://technet.microsoft.com/).
-   Não use uma ferramenta de reempacotamento para converter um pacote de Windows Installer em um novo pacote. O Windows Installer adiciona informações de configuração ao sistema, bem como recursos do aplicativo. Quando uma ferramenta de reempacotamento compara o sistema antes e depois da instalação, o reempacotador interpreta incorretamente as informações de configuração como parte do aplicativo. Isso geralmente danifica o aplicativo reempacotado. Em vez disso, use [transformações de personalização](a-customization-transform-example.md) para modificar um pacote de Windows Installer existente ou criar um novo pacote. Você pode criar transformações de personalização usando a ferramenta de [Msitran.exe](msitran-exe.md) .
-   Não use uma ferramenta de reempacotamento para consolidar vários pacotes Windows Installer em um único pacote. Em vez disso, você pode usar a ferramenta [Msistuff.exe](msistuff-exe.md) para configurar o executável de inicialização Setup.exe para instalar os pacotes um após o outro.
-   Faça seu pacote de Windows Installer para que ele possa ser facilmente personalizado pelo cliente. As variáveis globais usadas pelo Windows Installer durante uma instalação podem ser definidas usando [Propriedades](properties.md) públicas ou [transformações de personalização](a-customization-transform-example.md). Forneça a documentação para o uso dessas propriedades e valores padrão práticos para todos os valores personalizáveis. Para obter informações sobre como obter e definir propriedades, consulte [usando Propriedades](using-properties.md). Para obter um exemplo de uma transformação de personalização, consulte [um exemplo de transformação personalização](a-customization-transform-example.md).

## <a name="do-not-try-to-replace-protected-resources"></a>Não tente substituir os recursos protegidos.

Windows Installer pacotes não devem tentar substituir os recursos protegidos durante a instalação ou atualização. O Windows Installer não remove ou substitui esses recursos porque o Windows impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais. A proteção desses recursos impede falhas de aplicativos e do sistema operacional.

-   Quando executado no Windows Server 2008 ou no Windows Vista, o Windows Installer ignora a instalação de qualquer arquivo ou chave do Registro protegido pelo [proteção de recursos do Windows](../wfp/windows-resource-protection-portal.md) (WRP), o instalador insere um aviso no arquivo de log e continua com o restante da instalação sem erro. Para obter informações, consulte [usando Windows Installer e proteção de recursos do Windows](windows-resource-protection-on-windows-vista.md).
-   WRP é o novo nome da WFP (proteção de arquivo do Windows). A WRP protege chaves e pastas do registro, bem como arquivos essenciais do sistema. No Windows Server 2003, Windows XP e Windows 2000, quando o Windows Installer encontrou um arquivo protegido por WFP, o instalador solicitaria que a WFP instalasse o arquivo. Para obter informações, consulte [usando Windows Installer e proteção de recursos do Windows](windows-resource-protection-on-windows-vista.md).

## <a name="do-not-depend-upon-non-critical-resources"></a>Não dependa de recursos não críticos.

Sua instalação ou atualização não deve depender da instalação de recursos não críticos pelos seguintes motivos.

-   Ações personalizadas poderão falhar se dependerem de um componente que pertence a um recurso que o usuário anuncia em vez de instalar.
-   Ações personalizadas sequenciadas antes da ação [InstallFinalize](installfinalize-action.md) podem falhar se dependerem de um componente que contém um assembly que está sendo instalado. O Windows Installer não confirma assemblies para o GAC (cache de assembly global) até que a ação InstallFinalize seja concluída.

## <a name="use-the-api-to-retrieve-windows-installer-configuration-information"></a>Use a API para recuperar Windows Installer informações de configuração.

A instalação do seu aplicativo ou atualização não deve depender do acesso direto às informações de configuração do Windows Installer salvas no seu computador. Em vez disso, use a interface de programação de aplicativo Windows Installer para recuperar informações de configuração. O local e o formato das informações de configuração são gerenciados pelo serviço de Windows Installer e podem ser alterados.

-   As funções de instalação e configuração da API Windows Installer são descritas na [referência da função do instalador](installer-function-reference.md).
-   As [Propriedades de configuração](property-reference.md) são descritas na referência de propriedade.
-   Os métodos e as propriedades de automação são descritos na [referência da interface de automação](automation-interface-reference.md). O script de exemplo WiLstPrd.vbs se conecta a um objeto do instalador e enumera os produtos registrados e as informações do produto. Para obter informações, consulte [listar produtos, propriedades, recursos e componentes](list-products-properties-features-and-components.md).

## <a name="organize-the-installation-of-your-application-around-components"></a>Organize a instalação do seu aplicativo com base em componentes.

O serviço de Windows Installer instala ou remove coleções de recursos conhecidos como [componentes](windows-installer-components.md)do. Como os componentes são normalmente compartilhados, o autor de um pacote de instalação deve seguir as regras ao especificar os componentes de um recurso ou aplicativo.

-   Siga as regras de componente ao [organizar aplicativos em componentes](organizing-applications-into-components.md) para garantir que novos componentes ou novas versões de componentes possam ser instalados e removidos sem danificar outros aplicativos. Você pode seguir o procedimento descrito em [definindo componentes do instalador](defining-installer-components.md).
-   O instalador rastreia todos os componentes pelo respectivo GUID de ID de componente especificado na [tabela de componentes](component-table.md). É essencial para a operação do Windows Installer mecanismo de contagem de referência que o GUID de ID de componente está correto. Siga as diretrizes em [alterando o código do componente](changing-the-component-code.md).
-   Se o pacote precisar interromper as regras de componente, lembre-se das possíveis conseqüências e certifique-se de que a instalação nunca instala esses componentes, onde eles podem danificar os componentes no sistema do usuário. Para obter informações, consulte [o que acontece se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md).
-   Lembre-se de como o Windows Installer aplica as [regras de controle de versão do arquivo](file-versioning-rules.md) ao [substituir os arquivos existentes](replacing-existing-files.md). O Windows Installer primeiro determina se o arquivo de chave do componente já está instalado antes de tentar instalar qualquer um dos arquivos do componente. Se o instalador encontrar um arquivo com o mesmo nome que o arquivo de chave do componente instalado no local de destino, ele compara a versão, a data e o idioma dos dois arquivos de chave e usa regras de controle de versão de arquivo para determinar se deseja instalar o componente fornecido pelo pacote. Se o instalador determinar que precisa substituir a base do componente no arquivo de chave, ele usará as regras de controle de versão de arquivo em cada arquivo instalado para determinar se deseja substituir o arquivo.

## <a name="reduce-the-size-of-large-windows-installer-packages"></a>Reduza o tamanho de pacotes de Windows Installer grandes.

Pacotes muito grandes do Windows pegam recursos do sistema e podem ser difíceis de instalar para os usuários. É uma boa prática reduzir o tamanho de pacotes de Windows Installer muito grandes pelos métodos a seguir.

-   Compacte os arquivos na instalação e armazene-os em um arquivo de gabinete (. cab). O instalador permite que o arquivo. cab seja armazenado como um arquivo externo separado ou como um fluxo de dados no próprio pacote MSI. Para obter informações [, consulte usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).
-   Remova o espaço de armazenamento desperdiçado no arquivo. msi usando uma das opções discutidas em [reduzindo o tamanho de um arquivo. msi](reducing-the-size-of-an--msi-file.md).
-   Se seu pacote de Windows Installer contiver mais de 32767 arquivos, você deverá alterar o esquema do banco de dados. Para obter informações, consulte [criando um pacote grande](authoring-a-large-package.md).

## <a name="if-you-use-custom-actions-follow-good-custom-action-practices"></a>Se você usar ações personalizadas, siga as boas práticas de ação personalizadas.

O Windows Installer tem muitas [ações padrão](standard-actions-reference.md) internas para a instalação e manutenção de aplicativos. Os desenvolvedores devem tentar confiar nas ações padrão tanto quanto práticas, em vez de criar suas próprias [ações personalizadas](custom-actions.md). No entanto, há situações em que o desenvolvedor de um pacote de instalação descobre que é necessário gravar uma ação personalizada.

-   Siga as diretrizes para [usar ações personalizadas](using-custom-actions.md).
-   Siga as [diretrizes para proteger as ações personalizadas](guidelines-for-securing-custom-actions.md). As ações personalizadas que usam informações confidenciais não devem gravar essas informações no log. Para obter informações, consulte [segurança de ação personalizada](custom-action-security.md).
-   As ações personalizadas não devem tentar definir um ponto de entrada de restauração do sistema de dentro de uma ação personalizada. Para obter informações, consulte [definindo um ponto de restauração de uma ação personalizada](setting-a-restore-point-from-a-custom-action.md).
-   Retornar mensagens de erro de ações personalizadas e gravá-las no log para facilitar a solução de problemas de ações personalizadas. Para obter informações, consulte [ações de mensagens de erro personalizadas](error-message-custom-actions.md) e [retornando mensagens de erro de ações personalizadas](returning-error-messages-from-custom-actions.md).
-   Não altere o estado do sistema de uma ação personalizada imediata. Ações personalizadas que alteram o sistema diretamente ou chamam outro serviço do sistema devem ser adiadas para a hora em que o script de instalação é executado. Cada [ação personalizada de execução adiada](deferred-execution-custom-actions.md) que altera o estado do sistema deve ser precedida por uma [ação personalizada de reversão](rollback-custom-actions.md) para desfazer a alteração do estado do sistema em uma reversão de instalação. Para obter informações, consulte [alterando o estado do sistema usando uma ação personalizada](changing-the-system-state-using-a-custom-action.md).
-   As ações personalizadas que executam operações complexas de instalação devem ser um [arquivo executável](executable-files.md) ou uma [biblioteca de vínculo dinâmico](dynamic-link-libraries.md). Limite o uso de ações personalizadas com base em [scripts](scripts.md) para operações de instalação simples.
-   Faça os detalhes do que sua ação personalizada faz para o sistema facilmente detectável para administradores do sistema. Coloque os detalhes das entradas e dos arquivos de registro usados por sua ação personalizada em uma tabela personalizada e faça com que a ação personalizada seja lida desta tabela. Isso é demonstrado pelo exemplo no [uso de uma ação personalizada para criar contas de usuário em um computador local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md). Para obter informações sobre como adicionar tabelas personalizadas a um banco de dados, consulte [trabalhando com consultas](working-with-queries.md) e [exemplos de consultas de banco de dados usando o SQL e o script](examples-of-database-queries-using-sql-and-script.md).
-   Uma ação personalizada não deve exibir uma caixa de diálogo. As ações personalizadas que exigem uma interface do usuário podem usar a função [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) em vez disso. Consulte [enviando mensagens para Windows Installer usando o MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).
-   As ações personalizadas não devem usar nenhuma das funções listadas na página: [funções não para uso em ações personalizadas](functions-not-for-use-in-custom-actions.md).
-   Se a instalação for destinada a ser executada em um servidor de terminal, teste se todas as suas ações personalizadas podem ser executadas em um servidor de terminal. Para obter mais informações, consulte Propriedade [**TerminalServer**](terminalserver.md) .
-   Para que uma ação personalizada seja executada quando um patch específico é desinstalado, a ação personalizada deve estar presente no aplicativo original ou estar em um patch para o produto que sempre é aplicado. Para obter mais informações, consulte [correção de ações personalizadas de desinstalação de patch](patch-uninstall-custom-actions.md).
-   As ações personalizadas não devem usar o nível de interface do usuário como uma condição para enviar mensagens de erro ao instalador, pois isso pode interferir no registro em log e mensagens externas. Para obter informações, consulte [determinando o nível da interface do usuário de uma ação personalizada](determining-ui-level-from-a-custom-action.md).
-   Use instruções condicionais e [sintaxe de instrução condicional](conditional-statement-syntax.md) para garantir que o pacote execute corretamente as ações personalizadas, não execute ações personalizadas ou execute uma ação personalizada alternativa quando o pacote for desinstalado. Teste se o pacote funciona conforme o esperado ao [desinstalar ações personalizadas](uninstalling-custom-actions.md). Para obter informações, consulte [ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md)
-   Se a instalação deve ser capaz de ser executada por usuários que não têm privilégios de administrador, teste para garantir que todas as ações personalizadas possam ser executadas com privilégios de não administrador. Ações personalizadas exigem privilégios elevados para modificar partes do sistema que não são específicas do usuário. O instalador pode executar ações personalizadas com privilégios elevados se um aplicativo gerenciado estiver sendo instalado ou se a política do sistema tiver sido especificada para privilégios elevados. Todas as ações personalizadas que exigem privilégios elevados devem incluir a ação personalizada msidbCustomActionTypeInScript e msidbCustomActionTypeNoImpersonate [In-Script opções de execução](custom-action-in-script-execution-options.md) no tipo de ação personalizada. Isso é demonstrado pelo exemplo no [uso de uma ação personalizada para criar contas de usuário em um computador local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md).

## <a name="if-you-use-assemblies-follow-good-assembly-practices"></a>Se você usar assemblies, siga as práticas de assembly adequadas

Se o pacote usar [assemblies](assemblies.md)de software, siga as diretrizes para [adicionar assemblies a um pacote](adding-assemblies-to-a-package.md), [Atualizar assemblies](updating-assemblies.md)e [instalar e remover assemblies](installing-and-removing-assemblies.md).

## <a name="do-not-ship-concurrent-installations"></a>Não envie instalações simultâneas.

[Instalações simultâneas](concurrent-installations.md), também chamadas de instalações aninhadas, instalam outro pacote de Windows Installer durante uma instalação atualmente em execução. O uso de instalações simultâneas não é uma boa prática, pois elas são difíceis de atender aos clientes. A aplicação de patches e a atualização podem não funcionar com instalações simultâneas. A alternativa recomendada ao uso de instalações simultâneas é usar um aplicativo de instalação e um manipulador de interface de usuário externo para instalar vários pacotes de Windows Installer em sequência.

Para obter mais informações sobre como usar um manipulador de interface do usuário externo, consulte [monitorando uma instalação usando o MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md). Para obter mais informações sobre como usar um manipulador externo baseado em registro, consulte [monitorando uma instalação usando o MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md).

As instalações simultâneas, às vezes, são usadas em ambientes corporativos controlados para instalar aplicativos que não são destinados ao público. Siga estas diretrizes se você decidir usar instalações simultâneas.

-   Não use instalações simultâneas para instalar ou atualizar um produto de remessa.
-   Instalações simultâneas não devem compartilhar componentes.
-   Uma instalação administrativa não deve conter uma instalação simultânea.
-   As ProgressBars integradas não devem ser usadas com instalações simultâneas.
-   Os recursos que devem ser anunciados não devem ser instalados por uma instalação simultânea.
-   Um pacote que executa uma instalação simultânea de um aplicativo também deve desinstalar o aplicativo simultâneo quando o produto pai é desinstalado. Existe uma instalação aninhada no contexto do produto pai em Adicionar ou remover programas no painel de controle.

## <a name="keep-package-names-and-package-codes-consistent"></a>Mantenha os nomes de pacote e os códigos de pacote consistentes.

O arquivo. msi pode receber qualquer nome que ajude os usuários a identificar o pacote, mas o nome não deve ser alterado sem alterar também o código do produto.

-   Dê ao seu arquivo. msi um nome amigável que permita ao usuário identificar o conteúdo do pacote de Windows Installer.
-   O [código do produto](product-codes.md) é a identificação principal de um aplicativo e deve ser alterado sempre que houver uma atualização abrangente para o aplicativo. Para obter informações, consulte [**ProductCode**](productcode.md) e [alterando o código do produto](changing-the-product-code.md). Alterar o nome do arquivo. msi do aplicativo é considerado uma alteração abrangente e sempre requer uma alteração correspondente do código do produto para manter a consistência.
-   O [código do pacote](package-codes.md) é o identificador principal usado pelo instalador para pesquisar e validar o pacote correto para uma determinada instalação. Dois arquivos. msi não idênticos já devem ter o mesmo código de pacote. Se um pacote for alterado sem alterar o código do pacote, o instalador não poderá usar o pacote mais recente se ambos ainda estiverem acessíveis ao instalador. O código do pacote é armazenado na propriedade [**Resumo do número de revisão**](revision-number-summary.md) do fluxo de informações de [Resumo](summary-information-stream.md).
-   Observe que as letras no código do produto e nos [GUIDs](guid.md) de código do pacote devem ser maiúsculas.

## <a name="do-not-use-the-selfreg-and-typelib-tables"></a>Não use as tabelas SelfReg e TypeLib.

-   Os autores do pacote de instalação são altamente aconselhados em relação ao uso do auto-registro e da tabela [selfreg](selfreg-table.md) . Em vez disso, eles devem registrar módulos criando uma ou mais das tabelas no [grupo tabelas do registro](registry-tables-group.md). Muitos dos benefícios da Windows Installer são perdidos com o auto-registro porque as rotinas de Autoregistro tendem a ocultar informações de configuração críticas. Para obter uma lista dos motivos para evitar o auto-registro, consulte a [tabela selfreg](selfreg-table.md).
-   Os autores do pacote de instalação são altamente aconselhados em relação ao uso da tabela [TypeLib](typelib-table.md) . Em vez de usar a tabela TypeLib, registre bibliotecas de tipos usando a tabela [do registro](registry-table.md) . Se uma instalação que usa a tabela TypeLib falhar e precisar ser revertida, a reversão poderá não restaurar o computador para o mesmo estado que existia antes da reversão.

## <a name="provide-the-option-to-install-without-a-user-interface"></a>Forneça a opção para instalar sem uma interface do usuário.

Os administradores geralmente preferem implantar aplicativos dentro de uma empresa sem exigir interação do usuário. É uma boa prática habilitar seu aplicativo para fornecer a opção de ser instalada com o [nível de interface do usuário](user-interface-levels.md) de nenhum.

-   Use [Propriedades públicas](public-properties.md) para obter informações de configuração. Os administradores podem fornecer essas informações na linha de comando.
-   Não exija que a instalação dependa das informações coletadas da interação do usuário com caixas de diálogo. Essas informações não estão disponíveis durante uma instalação silenciosa.
-   Não reinicie automaticamente o computador do usuário durante uma instalação silenciosa.
-   Os administradores podem definir o [nível de interface do usuário](user-interface-levels.md) ao instalar o usando a opção de linha de [comando](command-line-options.md) "/q". O nível da interface do usuário também pode ser definido programaticamente com uma chamada para [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).

## <a name="avoid-using-the-alwaysinstallelevated-policy"></a>Evite usar a política AlwaysInstallElevated.

Se a política [AlwaysInstallElevated](alwaysinstallelevated.md) não estiver definida, os aplicativos não distribuídos pelo administrador serão instalados usando os privilégios do usuário e somente os aplicativos gerenciados terão privilégios elevados. Definir essa política direciona Windows Installer para usar permissões do sistema ao instalar o aplicativo no sistema. Esse método pode abrir um computador para um risco de segurança, porque quando essa política é definida, um usuário não administrador pode executar instalações com privilégios [*elevados*](e-gly.md) e acessar locais seguros no computador. É uma boa prática usar outro método do que a política de AlwaysInstallElevated ao [instalar um pacote com privilégios elevados para um não administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md) ou [aplicação de patches Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).

## <a name="enable-the-disablemedia-policy-to-limit-unauthorized-installation"></a>Habilite a política DisableMedia para limitar a instalação não autorizada.

A política [DisableMedia](disablemedia.md) pode impedir a instalação não autorizada de aplicativos. Quando essa política está habilitada, os usuários e administradores que executam uma instalação de manutenção de um produto são impedidos de usar a caixa de diálogo de procura para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis. Procurar outros produtos é impedido, independentemente de a instalação ser feita com privilégios elevados. Ainda é possível que o usuário reinstale o produto da mídia se o usuário tiver uma origem de mídia rotulada corretamente.

## <a name="keep-the-original-package-source-files-secure-and-available-to-users"></a>Mantenha os arquivos de origem do pacote original seguros e disponíveis para os usuários.

Em alguns casos, a origem original do pacote de Windows Installer pode ser necessária para instalar-sob demanda, reparar ou atualizar um aplicativo. Se o instalador não conseguir localizar uma fonte disponível, será solicitado que o usuário forneça a mídia ou vá para um local de rede que contenha as fontes necessárias. É uma boa prática garantir que o instalador tenha as fontes necessárias sem precisar solicitar o usuário.

-   Use [assinaturas digitais e arquivos de gabinete externo](digital-signatures-and-external-cabinet-files.md) para garantir que as origens de origem usadas pelo instalador sejam seguras. Uma imagem de origem não compactada armazenada em um local público não é segura.
-   Inclua uma lista completa de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo na propriedade [**SourceList**](sourcelist.md) .
-   Use um compartilhamento de Sistema de Arquivos Distribuído (DFS) para o caminho de origem.
-   Use a API Windows Installer para recuperar e modificar informações de lista de origem para aplicativos e patches de Windows Installer. Para obter informações, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).
-   Use os métodos e as propriedades do [**objeto do instalador**](installer-object.md), [**objeto de produto**](product-object.md)e [**objeto de patch**](patch-object.md) para recuperar e modificar informações de lista de origem para aplicativos Windows Installer e patches.
-   Siga os pontos listados em [impedindo que um patch requeira acesso aos pontos de origem de instalação originais](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md) para minimizar a possibilidade de o patch precisar de acesso às fontes originais.
-   Armazene os arquivos de origem do pacote em um local que não seja a pasta temporária do sistema. Windows Installer arquivos de origem armazenados na pasta temporária podem ficar indisponíveis para os usuários.

## <a name="enable-verbose-logging-on-users-computer-when-troubleshooting-deployment"></a>Habilite o log detalhado no computador do usuário ao solucionar problemas de implantação.

[Windows Installer log](windows-installer-logging.md) inclui uma opção de log detalhado que pode ser habilitada no computador de um usuário. As informações em um log detalhado podem ser úteis ao tentar solucionar problemas de implantação de pacote Windows Installer.

-   Você pode habilitar o log detalhado no computador do usuário usando [Opções de linha de comando](command-line-options.md), a propriedade [**MsiLogging**](msilogging.md) , a política de [registro em log](logging.md), o [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)e o método [**EnableLog**](installer-enablelog.md) .
-   Um recurso muito útil para interpretar Windows Installer arquivos de log é [Wilogutl.exe](wilogutl-exe.md). Essa ferramenta ajuda a análise de arquivos de log e exibe soluções sugeridas para erros encontrados em um arquivo de log.
-   Para obter mais informações sobre como interpretar Windows Installer arquivos de log, consulte a white paper disponível no site do TechNet: [Windows Installer: benefícios e implementação para administradores do sistema](https://www.microsoft.com/technet/prodtechnol/windows2000serv/maintain/featusability/winmsi.mspx).
-   A opção de log detalhado deve ser usada somente para fins de solução de problemas e não deve ser deixada porque pode ter efeitos adversos no desempenho do sistema e no espaço em disco. Cada vez que você usa a ferramenta Adicionar/remover programas no painel de controle, um novo arquivo é criado.

## <a name="uninstallation-leaves-the-users-computer-in-a-clean-state"></a>A desinstalação deixa o computador do usuário em um estado limpo.

A remoção do aplicativo é tão importante quanto a instalação. Quando um pacote de Windows Installer é desinstalado, ele não deve deixar nenhuma parte inútil dele atrás no computador do usuário.

-   Se um arquivo que deveria ter sido removido do computador do usuário permanecer instalado após a execução de uma desinstalação, talvez o instalador não esteja removendo o componente que contém o arquivo por um ou mais dos motivos descritos em [removendo arquivos perdidos](removing-stranded-files.md).
-   Se um aplicativo precisar ser registrado, crie o pacote para remover informações do registro quando o aplicativo for desinstalado. Para obter informações, consulte [adicionando ou removendo chaves do registro na instalação ou remoção de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). Se um aplicativo não estiver registrado, o aplicativo não estará listado no recurso Adicionar ou remover programas no painel de controle e não poderá ser gerenciado usando o Windows Installer.
-   Para ocultar um aplicativo do recurso Adicionar ou remover programas no painel de controle e ainda poder usar o Windows Installer para gerenciar o aplicativo, siga as diretrizes descritas em [adicionando e removendo um aplicativo e não deixando nenhum rastreamento no registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).
-   As ações personalizadas devem ser condicionadas para serem executadas ou não, conforme necessário, após a desinstalação. Diferentes ações personalizadas talvez precisem ser executadas na instalação e na desinstalação.
-   As informações de personalização específicas do usuário podem ser armazenadas em um arquivo de texto no computador. Isso tem a vantagem de que o arquivo pode ser removido quando o aplicativo é desinstalado, mesmo que o usuário dessa personalização não esteja conectado no momento.

## <a name="test-packages-for-both-per-user-and-per-machine-installation-deployment"></a>Pacotes de teste para a implantação de instalação por usuário e por computador.

É uma boa prática permitir que os clientes decidam se deseja implantar um pacote para instalação no [contexto de instalação](installation-context.md)por computador ou por usuário.

-   Considere se o aplicativo deve estar disponível somente para usuários específicos ou para todos os usuários do computador durante o processo de desenvolvimento.
-   Teste se o pacote funciona corretamente para a instalação por usuário e contextos de instalação por máquina.
-   Torne o pacote facilmente personalizável e permita que os clientes decidam se desejam implantá-los por usuário ou por computador.

## <a name="plan-and-test-a-servicing-strategy-before-shipping-the-application"></a>Planeje e teste uma estratégia de serviço antes de enviar o aplicativo.

Você deve decidir como pretende atender o aplicativo antes de implantar o aplicativo pela primeira vez.

-   Considere os tipos de atualizações que você pretende usar para atender seu aplicativo no futuro. O Windows Installer fornece três tipos de atualizações: [atualização pequena](small-updates.md), [atualização secundária](minor-upgrades.md)e [atualizações principais](major-upgrades.md). As diferenças entre eles são descritas no tópico [patches e atualizações](patching-and-upgrades.md) .
-   Antes de enviar seu aplicativo, teste se ele funciona conforme o esperado após a manutenção com cada tipo de atualização.

## <a name="reduce-the-dependency-of-updates-upon-the-original-sources"></a>Reduza a dependência de atualizações nas fontes originais.

Se os arquivos de origem originais forem necessários para atualizar seu aplicativo, isso poderá dificultar a manutenção do aplicativo. Os métodos a seguir podem ajudar a reduzir a dependência de atualizações nas fontes originais.

-   Use um [*patch Delta*](d-gly.md) para atualizar as versões de linha de base do seu aplicativo, como a versão RTM e as versões de Service Pack. Siga as diretrizes para usar os patches Delta descritos no tópico: [reduzindo o tamanho do patch](reducing-patch-size.md).
-   Siga as recomendações listadas no tópico: [impedir que um patch exija acesso à fonte de instalação original](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

## <a name="do-not-distribute-unserviceable-merge-modules"></a>Não distribua módulos de mesclagem sem serviço.

Os aplicativos não devem depender de [módulos de mesclagem](merge-modules.md) para a instalação do componente se o proprietário do módulo de mesclagem e o proprietário do aplicativo forem diferentes. Isso pode dificultar o serviço do aplicativo porque ambos os proprietários precisam coordenar para atualizar o aplicativo ou o módulo. Sem conhecer todos os aplicativos que usaram o módulo de mesclagem, o proprietário do aplicativo não é capaz de atualizar o módulo de mesclagem sem arriscar que a atualização possa ser incompatível com outro aplicativo. O proprietário do módulo de mesclagem não tem nenhum método direto para atualizar Windows Installer pacotes que já instalaram o módulo de mesclagem.

-   Considere fornecer os componentes necessários aos usuários como outro Windows Installer instalação.

## <a name="avoid-patching-administrative-installations"></a>Evite aplicar patches em instalações administrativas.

Forneça em uma rede uma [instalação administrativa](administrative-installation.md) do pacote de Windows Installer original do seu aplicativo para permitir que os membros de um grupo de trabalho instalem o aplicativo. Os usuários dessa imagem administrativa devem aplicar atualizações à instância local do aplicativo localizado em seu computador. Isso mantém os usuários em sincronia com a imagem administrativa. Não é recomendável aplicar atualizações à instalação administrativa pelos seguintes motivos.

-   O tamanho e a latência do download necessários para que os usuários obtenham uma atualização são aumentados em comparação com o download de um patch. Todo o pacote de Windows Installer e arquivos de origem atualizados devem ser baixados, rearmazenados em cache e reinstalados.
-   Os usuários não podem fazer a [instalação sob demanda](installation-on-demand.md) e reparar aplicativos de uma instalação administrativa atualizada até que eles rearmazenem novamente em cache e reinstalem o aplicativo.
-   A aplicação de um patch a uma instalação administrativa remove a assinatura digital do pacote. Um administrador deve desistir do pacote. Para obter mais informações sobre como usar assinaturas digitais, consulte [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).
-   Muitos patches binários visam a imagem RTM do aplicativo e exigem uma versão de arquivo anterior. A instância local de um aplicativo instalado de uma instalação administrativa atualizada pode não funcionar com outras atualizações. Muitos aplicativos de patch binários podem falhar.
-   A aplicação de um patch a uma instalação administrativa atualiza os arquivos de origem e o arquivo. msi, mas não carimba a imagem de rede com informações sobre a atualização. Os usuários não podem determinar quais atualizações foram recebidas da instalação administrativa. Isso torna impossível sequenciar as atualizações aplicadas no lado do usuário com aquelas já aplicadas no lado da imagem administrativa.
-   Os patches aplicados a uma instalação administrativa não são [patches desinstaláveis](uninstallable-patches.md). Isso pode impedir que o código do pacote em cache no computador do usuário se torne diferente do código do pacote na instalação administrativa. Se o código do pacote armazenado em cache no computador do usuário se tornar diferente daquele na instalação administrativa, reinstale o aplicativo da instalação administrativa e, em seguida, corrija o computador cliente.
-   Se você decidir aplicar pequenas atualizações por meio da aplicação de patch em uma imagem administrativa, siga as diretrizes descritas no tópico: [aplicando pequenas atualizações por meio da aplicação de patch em uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md).

## <a name="register-updates-to-run-with-elevated-privilege"></a>Registre as atualizações para executar com privilégios elevados.

A partir do Windows Installer 3,0, é possível aplicar patches a um aplicativo que foi instalado em um contexto gerenciado por usuário, depois que o patch tiver sido registrado como tendo privilégios elevados. Você não pode aplicar patches a aplicativos que estão instalados em um contexto gerenciado por usuário usando versões do Windows Installer anteriores à versão 3,0.

-   Use o método [**SourceListAddSource**](patch-sourcelistaddsource.md) ou a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para registrar um pacote de patch como tendo privilégios elevados. Siga as diretrizes e os exemplos fornecidos na [aplicação de patches Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).
-   Ao executar Windows Installer versão 4,0 no Windows Vista, você também pode usar a [aplicação de patches de controle de conta de usuário (UAC)](user-account-control--uac--patching.md) para permitir que os autores de instalações de Windows Installer identifiquem patches assinados digitalmente que podem ser aplicados no futuro por usuários não administradores. Isso só está disponível com a instalação de pacotes no [contexto de instalação](installation-context.md) por máquina (AllUsers = 1).
-   Verifique se a aplicação de patches com privilégios mínimos não foi desabilitada definindo a propriedade [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) ou a política [DisableLUAPatching](disableluapatching.md) .

## <a name="use-the-msipatchsequence-table-to-sequence-patches"></a>Use a tabela MsiPatchSequence para sequenciar patches.

Inclua uma [tabela MsiPatchSequence](msipatchsequence-table.md) em seu pacote e adicione informações de sequenciamento de patch. A partir do Windows Installer versão 3,0, o instalador pode usar a tabela MsiPatchSequence ao [instalar vários patches](installing-multiple-patches.md) para determinar a melhor sequência de aplicativos de patch. Use as diretrizes descritas no [sequenciamento de patches no Windows Installer versão 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3) White Paper para definir as famílias de patches.

-   Se for prático, especifique todos os patches como pertencentes a uma única família de patches. Em muitos casos, uma única família de patches fornece flexibilidade suficiente para os patches de sequência. A complexidade da criação aumenta quando várias famílias de patches são usadas. Atribua um nome significativo à família de patches e atribua valores de sequência na família de patches que aumentam ao longo do tempo. Siga o [exemplo de várias correções](multiple-patching-example.md) para aplicar patches na ordem em que foram emitidos.
-   Use a [tabela PatchSequence](patchsequence-table--patchwiz-dll-.md) em [Patchwiz.dll](patchwiz-dll.md) para gerar as informações na [tabela MsiPatchSequence](msipatchsequence-table.md). A versão do PATCHWIZ.DLL lançada com Windows Installer 3,0 pode gerar automaticamente informações de sequenciamento de patch. Para obter mais informações sobre como adicionar um novo patch, consulte [gerando informações de sequência de patch](generating-patch-sequence-information---patchwiz-dll-.md). Para obter mais informações sobre cenários de sequenciamento de patch, consulte o White Paper: [sequenciamento de patch no Windows Installer versão 3,0](https://www.microsoft.com/downloads/details.aspx?FamilyID=ad7ac91e-2493-4549-ae6f-bf5e007c12a3).

## <a name="test-the-installation-package-thoroughly"></a>Teste o pacote de instalação completamente.

Teste a instalação, o reparo e a remoção corretas do pacote de Windows Installer. Você pode dividir seu processo de teste nas seguintes partes.

-   Teste de instalação – teste a instalação com todas as combinações possíveis de recursos de aplicativo. Testar todos os tipos de instalação, incluindo a [instalação administrativa](administrative-installation.md), a [reversão da instalação](rollback-installation.md)e [a instalação sob demanda](installation-on-demand.md). Experimente todos os possíveis métodos de instalação, incluindo o clique no arquivo. msi, nas [Opções de linha de comando](command-line-options.md)e na instalação no painel de controle. Teste se o pacote pode ser instalado por usuários em todos os possíveis contextos de privilégio. Tente instalar o pacote depois que ele tiver sido implantado por todos os métodos possíveis. Habilite o [log de Windows Installer](windows-installer-logging.md) para cada teste e resolva todos os erros encontrados no log do instalador e no log de eventos.
-   Teste de interface do usuário-teste o pacote quando instalado com todos os [níveis de interface do usuário](user-interface-levels.md)possíveis. Teste o pacote instalado sem interface do usuário e com todas as informações fornecidas por meio da interface do usuário. Verifique a [acessibilidade](accessibility.md) da interface do usuário e se a interface do usuário funciona como esperado para diferentes resoluções de tela e tamanhos de fonte.
-   Manutenção e reparo de teste – teste se o pacote pode lidar com [patches e atualizações](patching-and-upgrades.md) entregues por uma [pequena atualização](small-updates.md), [atualização secundária](minor-upgrades.md)e [atualizações importantes](major-upgrades.md). Antes de implantar o pacote, grave uma atualização de avaliação de cada tipo e tente aplicá-lo ao pacote original.
-   Teste de desinstalação – Verifique se quando o pacote é removido ele não deixa nenhuma parte inútil de si mesmo no computador do usuário e se apenas as informações pertencentes ao pacote foram removidas. Reinicialize o computador de teste após desinstalar o pacote e verificar a integridade das ferramentas de sistema comuns e outros aplicativos padrão. Teste se o pacote pode ser removido por usuários em todos os possíveis contextos de privilégio. Teste todos os métodos para remover o pacote, clique no arquivo. msi, tente as [Opções de linha de comando](command-line-options.md)e tente remover o pacote do painel de controle. Habilite o [log de Windows Installer](windows-installer-logging.md) para cada teste e resolva todos os erros encontrados no log do instalador e no log de eventos.
-   Teste de funcionalidade do produto – Verifique se o aplicativo funciona conforme o esperado após a instalação, o reparo ou a remoção do pacote.

## <a name="fix-all-validation-errors-before-deploying-a-new-or-revised-installation-package"></a>Corrija todos os erros de validação antes de implantar um pacote de instalação novo ou revisado.

Execute a [validação de pacote](package-validation.md) em um pacote de Windows Installer novo ou revisado antes de tentar instalá-lo pela primeira vez. A validação verifica se há erros na criação do banco de dados Windows Installer. A tentativa de instalar um pacote que não passe na validação pode danificar o sistema do usuário.

-   Você pode validar seu pacote usando [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md). Ambas as ferramentas são fornecidas com o SDK do Windows. Os fornecedores terceirizados também podem incorporar o sistema de validação ICE ao seu ambiente de criação.
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

 

 
