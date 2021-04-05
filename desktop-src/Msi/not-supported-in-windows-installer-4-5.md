---
description: O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer&\# 160; 4.5 e versões anteriores.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Sem suporte no Windows Installer 4,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d1d1b3039c4e51c7233f98ee2e41afb308a822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661561"
---
# <a name="not-supported-in-windows-installer-45"></a>Sem suporte no Windows Installer 4,5

O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 4,5 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso tenha suporte. Consulte a documentação principal para determinar qual versão de Windows Installer é necessária para um recurso específico. Para obter informações sobre outras versões do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).

O Windows Installer 4,5 está disponível como um pacote redistribuível para o Windows Server 2008, o Windows Vista com Service Pack 1 (SP1), o Windows XP com Service Pack 2 (SP2) e posterior e o Windows Server 2003 com Service Pack 1 (SP1) e posterior. Para obter uma lista completa de todas as versões e redistribuíveis do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Installer 4,5 e versões anteriores.

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
-   Suporte ao [controle de bitmap](bitmap-control.md) de formatos de arquivo de imagem WIC

[Avaliadores de consistência internos-ICEs](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interface de automação](automation-interface.md)

-   Propriedades do [ **objeto instalador**](installer-object.md)

    -   [**Installer. ClientsEx**](installer-clientsex.md)
    -   [**Installer. ComponentsEx**](installer-componentsex.md)
    -   [**Installer. ComponentPathEx**](installer-componentpathex.md)

-   Propriedades do [ **objeto de componente**](components.md)

    -   [**Component. ComponentCode**](component-componentcode.md)
    -   [**Component. UserId**](component-usersid.md)
    -   [**Componente. Context**](component-context.md)

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

Windows Installer 4,5 não oferece suporte a alguns recursos que permitem a instalação de um único pacote de instalação no contexto de instalação por computador ou por usuário. Para obter mais informações, consulte [criação de pacote único](single-package-authoring.md).

Windows Installer 4,5 não oferece suporte a algumas opções de configuração de serviços que podem habilitar um pacote para personalizar os [Serviços](../services/services.md) em um computador. Para obter mais informações, consulte [usando a configuração de serviços](using-services-configuration.md).

O Windows Installer 4,5 não oferece suporte a alguns recursos que permitem que o Windows Installer proteja novas contas, [Serviços](../services/services.md)do Windows, arquivos, pastas e chaves do registro. Para obter informações, consulte [Securing Resources](securing-resources-.md).

Windows Installer 4,5 não oferece suporte a alguns recursos que permitem que a instalação Enumere todos os componentes instalados no computador e obtenha o caminho da chave para o componente. Para obter mais informações, consulte [enumerando componentes](enumerating-components-.md).

 

 
