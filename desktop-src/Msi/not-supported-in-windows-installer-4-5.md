---
description: As funções, tabelas e propriedades do instalador Windows Windows listadas nesta página não têm suporte do Windows Installer&\# 160;4.5 e versões anteriores.
ms.assetid: 89662e62-53fb-4b50-8583-80518c6fda6d
title: Sem suporte no Windows 4.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a285094610f0a00a39a26bb2d0683cb41afdfa3ed126ac27f7655c3cd56df17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979346"
---
# <a name="not-supported-in-windows-installer-45"></a>Sem suporte no Windows 4.5

As Windows, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 4.5 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso seja suportado. Consulte a documentação principal para determinar qual Windows do Instalador é necessária para um recurso específico. Para obter informações sobre Windows versões do Instalador do [Windows .](what-s-new-in-windows-installer.md)

Windows O Instalador 4.5 está disponível como um redistribuível para o Windows Server 2008, Windows Vista com Service Pack 1 (SP1), Windows XP com Service Pack 2 (SP2) e posterior e Windows Server 2003 com Service Pack 1 (SP1) e posterior. Para ver uma lista completa de todas as versões Windows instalador e redistribuíveis, consulte Versões lançadas [do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Installer 4.5 e versões anteriores.

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

[Controlevents](control-events.md)

-   [MsiPrint ControlEvent](msiprint-controlevent.md)
-   [MsiLaunchApp ControlEvent](msilaunchapp-controlevent.md)

[Controles](controls.md)

-   [Controle de hiperlink](hyperlink-control.md)
-   [Suporte ao Controle de Bitmap](bitmap-control.md) de formatos de arquivo de imagem WIC

[Avaliadores de consistência interna – ICEs](internal-consistency-evaluators-ices.md)

-   [ICE102](ice-102.md)
-   [ICE103](ice-103.md)
-   [ICE104](ice-104.md)
-   [ICE105](ice-105.md)

[Interface de Automação](automation-interface.md)

-   Propriedades do [ **objeto do instalador**](installer-object.md)

    -   [**Installer.ClientsEx**](installer-clientsex.md)
    -   [**Installer.ComponentsEx**](installer-componentsex.md)
    -   [**Installer.ComponentPathEx**](installer-componentpathex.md)

-   Propriedades do [ **objeto component**](components.md)

    -   [**Component.ComponentCode**](component-componentcode.md)
    -   [**Component.UserSID**](component-usersid.md)
    -   [**Component.Context**](component-context.md)

-   Propriedades do [ **objeto de cliente**](client.md)

    -   [**Client.ProductCode**](client-productcode.md)
    -   [**Client.ComponentCode**](client-componentcode.md)
    -   [**Client.UserSID**](client-usersid.md)
    -   [**Client.Context**](client-context.md)

-   Propriedades do [**objeto ComponentInfo**](componentinfo.md)

    -   [**ComponentInfo.ComponentCode**](componentinfo-componentcode.md)
    -   [**ComponentInfo.Path**](componentinfo-path.md)
    -   [**ComponentInfo.State**](componentinfo-state.md)

## <a name="notes"></a>Observações

Windows O Instalador 4.5 não dá suporte a alguns recursos que permitem que um único pacote de instalação seja instalado no contexto de instalação por computador ou por usuário. Para obter mais informações, consulte [Single Package Authoring](single-package-authoring.md).

Windows O Instalador 4.5 não dá suporte a algumas opções de configuração de serviços que podem permitir que um pacote personalize os [serviços](../services/services.md) em um computador. Para obter mais informações, consulte [Using Services Configuration](using-services-configuration.md).

Windows O Instalador 4.5 não dá suporte a alguns recursos que permitem que o instalador do Windows proteja novas contas, Windows [serviços,](../services/services.md)arquivos, pastas e chaves do Registro. Para obter informações, consulte [Proteger recursos](securing-resources-.md).

Windows O Instalador 4.5 não dá suporte a alguns recursos que permitem que a instalação enumere todos os componentes instalados no computador e obtenham o caminho da chave para o componente. Para obter mais informações, consulte [Enumerando componentes](enumerating-components-.md).

 

 
