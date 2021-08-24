---
description: as informações neste tópico identificam as adições e alterações que estão disponíveis no Windows Installer&\# 160; 5.0.
ms.assetid: c088c15b-0eef-4a92-bb65-e7fe871afbfe
title: o que há de novo no Windows Installer 5,0
ms.topic: article
ms.date: 11/08/2019
ms.openlocfilehash: 82c6ae3bf5c6781ba84d18b366998c74deedd4ca0fa4c61ac452b1d0ec409850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145219"
---
# <a name="whats-new-in-windows-installer-50"></a>o que há de novo no Windows Installer 5,0

as informações neste tópico identificam as adições e alterações que estão disponíveis no Windows Installer 5,0.

Windows O instalador 5,0 está incluído nas seguintes versões do Windows:

* cliente: Windows 7 e todas as versões posteriores.
* servidor: Windows server 2008 R2 e todas as versões posteriores.

> [!NOTE]
> não há pacotes redistribuíveis para o Windows Installer 5,0. para obter uma lista de redistribuíveis disponíveis para versões anteriores do Windows Installer, consulte [Windows Installer redistribuíveis](windows-installer-redistributables.md). para obter uma lista completa de versões de Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

Esta página é fornecida como um guia para a documentação do. Você deve consultar a seção requisitos nas páginas de referência principais para determinar os requisitos reais do sistema operacional. as partes do Windows Installer que não estão vinculadas a esta página podem estar disponíveis em outra versão do Windows Installer. para obter informações sobre outras versões de Windows Installer, consulte [What ' s New in Windows Installer](what-s-new-in-windows-installer.md).

[Ações padrão](standard-actions.md)

-   [MsiConfigureServices](msiconfigureservices-action.md)

[Funções do instalador](installer-functions.md)

-   [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
-   [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
-   [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

[Tipos de dados de coluna](column-data-types.md)

-   [**FormattedSDDLText**](formattedsddltext.md)

[Propriedades](properties.md)

-   [**MSIFASTINSTALL**](msifastinstall.md)
-   [**MSIINSTALLPERUSER**](msiinstallperuser.md)

[Propriedades de informações de resumo](summary-information-stream-reference.md)

-   o [**resumo do modelo**](template-summary.md) tem novos valores para indicar que o banco de dados é compatível com Windows RT ou com a plataforma Arm64.

[Tabelas de banco de dados](database-tables.md)

-   [Tabela MsiServiceConfig](msiserviceconfig-table.md)
-   [Tabela MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md)
-   [Tabela MsiShortcutProperty](msishortcutproperty-table.md)
-   [Tabela MsiLockPermissionsEx](msilockpermissionsex-table.md)

[ControlEvents](control-events.md)

-   [MsiPrint ControlEvent,](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent,](msilaunchapp-controlevent.md)

[Controles](controls.md)

-   [Controle de hiperlink](hyperlink-control.md)

[Avaliadores de consistência internos-ICEs](internal-consistency-evaluators-ices.md)

-   [ICE101](ice-101.md)
-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interface de automação](automation-interface.md)

-   Propriedades do [ **objeto instalador**](installer-object.md)

    -   [**Installer. ClientsEx**](installer-clientsex.md)
    -   [**Installer. ComponentsEx**](installer-componentsex.md)
    -   [**Installer. ComponentPathEx**](installer-componentpathex.md)

-   Propriedades do [ **objeto componentes**](components.md)

    -   [**Components. ComponentCode**](component-componentcode.md)
    -   [**Components. UserId**](component-usersid.md)
    -   [**Components. Context**](component-context.md)

-   Propriedades do [ **objeto de cliente**](client.md)

    -   [**Client. ProductCode**](client-productcode.md)
    -   [**Client. ComponentCode**](client-componentcode.md)
    -   [**Client. UserId**](client-usersid.md)
    -   [**Cliente. contexto**](client-context.md)

-   Propriedades do objeto [**ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo. Path**](componentinfo-path.md)
    -   [**ComponentInfo. State**](componentinfo-state.md)

## <a name="notes"></a>Observações

os desenvolvedores de instalação podem usar o Windows Installer 5,0 para criar um único pacote de instalação compatível com a instalação por computador ou a instalação por usuário do aplicativo. Para obter mais informações, consulte [criação de pacote único](single-package-authoring.md). O avaliador de consistência interno [ICE105](ice-105.md) verifica se o pacote foi criado para ser instalado em um contexto por usuário. Um aplicativo capaz de ser instalado, atualizado, executado e removido por um usuário padrão sem elevação é chamado de aplicativo Per-User (PUA). Um PUA pode fornecer uma melhor experiência do usuário, minimizar efeitos no sistema e outros usuários do computador e reserva o prompt do UAC para situações que realmente exigem a elevação dos privilégios do usuário. os recursos de criação de pacote único do Windows Installer 5,0 podem facilitar o desenvolvimento de aplicativos Per-User.

as opções de configuração de serviços permitem que um pacote de Windows Installer personalize os [serviços](../services/services.md) em um computador. Para obter mais informações, consulte [usando a configuração de serviços](using-services-configuration.md).

a partir do Windows Installer 5,0, um pacote Windows Installer é capaz de proteger novas contas, Windows [serviços](../services/services.md), arquivos, pastas e chaves do registro. A tabela [MsiLockPermissionsEx](msilockpermissionsex-table.md) pode especificar um descritor de segurança que nega permissões, especifica a herança de permissões de um recurso pai ou especifica as permissões de uma nova conta. Para obter informações, consulte [Securing Resources](securing-resources-.md).

Windows O instalador 5,0 pode enumerar todos os componentes instalados no computador e obter o caminho de chave para o componente. Para obter mais informações, consulte [enumerando componentes](enumerating-components-.md).

Windows o instalador 5,0 em execução no Windows Server 2012 ou Windows 8 dá suporte à instalação de aplicativos aprovados no Windows RT. um pacote Windows Installer, patch ou transformação que não foi assinado pela Microsoft não pode ser instalado no Windows RT. A propriedade [**Summary do modelo**](template-summary.md) indica a plataforma que é compatível com o banco de dados de instalação e deve incluir o valor para Windows RT.

Windows o instalador 5,0 em execução no Windows 10 nos processadores Arm64 dá suporte à instalação de aplicativos compilados especificamente para a plataforma Arm64.  A propriedade [**Summary do modelo**](template-summary.md) desses pacotes precisa incluir o valor Arm64. 

 
