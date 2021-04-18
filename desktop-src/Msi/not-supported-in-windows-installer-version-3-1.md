---
description: O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer&\# 160; 3.1 e versões anteriores.
ms.assetid: fbf75dbe-3fa1-424b-83bb-cfd0b179107c
title: Sem suporte no Windows Installer 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a221d80f56c5737cc5ae92a040a005ae42449e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757382"
---
# <a name="not-supported-in-windows-installer-31"></a>Sem suporte no Windows Installer 3,1

O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 3,1 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso tenha suporte. Consulte a documentação principal para determinar qual versão de Windows Installer é necessária para um recurso específico. Para obter informações sobre outras versões do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,1 está disponível para o Windows Server 2003, Windows XP ou Windows 2000. Para obter uma lista de todas as versões e redistribuíveis do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Installer 3,1 e versões anteriores.

[Funções do instalador](installer-functions.md)

-   [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)

[Propriedades](properties.md)

-   [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)
-   [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md)
-   [**MSIDISABLERMRESTART**](msidisablermrestart.md)
-   [**MsiLogFileLocation**](msilogfilelocation.md)
-   [**MsiLogging**](msilogging.md)
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
-   [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)
-   [**MSIRMSHUTDOWN**](msirmshutdown.md)
-   [**MsiRunningElevated**](msirunningelevated-.md)
-   [**MsiSystemRebootPending**](msisystemrebootpending.md)
-   [**MsiTabletPC**](msitabletpc.md)
-   [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)

[Propriedades de informações de resumo](summary-information-stream-reference.md)

-   A [**propriedade de resumo contagem de palavras**](word-count-summary.md) tem novos bits de sinalizador para especificar se a instalação do pacote requer privilégios elevados.

[Política do sistema](system-policy.md)

-   [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
-   [DisableLoggingFromPackage](disableloggingfrompackage.md)

[Tabelas de banco de dados](database-tables.md)

-   [Tabela de atalho](shortcut-table.md)

    Novas colunas: DisplayResourceDLL, DisplayResourceId, DescriptionResourceDLL e DescriptionResourceId

[Caixas de diálogo](dialog-boxes.md)

-   [Caixa de diálogo MsiRMFilesInUse](msirmfilesinuse-dialog.md)

[Atributos de controle](control-attributes.md)

-   [ElevationShield](elevationshield-attribute.md)

[ControlEvents](control-events.md)

-   [RmShutdownAndRestart](rmshutdownandrestart-controlevent.md)

[Tipos de mensagem de interface do usuário externa](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)

-   INSTALLLOGMODE \_ RMFILESINUSE

[Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   atributo **msidbComponentAttributesDisableRegistryReflection** na [tabela de componentes](component-table.md)

[Interface de automação](automation-interface.md)

-   Métodos do [ **objeto instalador**](installer-object.md)

    -   [**Installer. AdvertiseProduct**](installer-advertiseproduct.md)
    -   [**Installer. AdvertiseScript**](installer-advertisescript.md)
    -   [**Installer. CreateAdvertiseScript**](installer-createadvertisescript.md)
    -   [**Installer. ProvideAssembly**](installer-provideassembly.md)

-   Propriedades do [ **objeto instalador**](installer-object.md)

    -   [**Installer. PatchFiles**](installer-patchfiles.md)
    -   [**Installer. ProductElevated**](installer-productelevated.md)
    -   [**Installer. ProductInfoFromScript**](installer-productinfofromscript.md)

## <a name="notes"></a>Observações

O serviço de Windows Installer deve ser executado no Windows Vista para habilitar o uso do [Gerenciador de reinicialização](../rstmgr/restart-manager-portal.md), o [*controle de conta de usuário*](u-gly.md)e a aplicação de [patches de UAC (controle de conta de usuário)](user-account-control--uac--patching.md). Para obter informações, consulte [usando Windows Installer com o Gerenciador de reinicialização](using-windows-installer-with-restart-manager.md) e [usando o Windows Installer com a](using-windows-installer-with-uac.md) [aplicação de patches UAC e UAC (controle de conta de usuário)](user-account-control--uac--patching.md).

O Windows Installer 3,1 dá suporte à WFP (proteção de arquivo do Windows) e não oferece suporte a Proteção de Recursos do Windows (WRP). A WRP no Windows Server 2008 e no Windows Vista substitui a WFP no Windows Server 2003, no Windows XP e no Windows 2000. Para obter informações sobre Windows Installer e WFP, consulte [usando Windows Installer e proteção de recursos do Windows](windows-resource-protection-on-windows-vista.md).

 

 
