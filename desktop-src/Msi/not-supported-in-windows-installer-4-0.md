---
description: O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer&\# 160; 4.0 e versões anteriores.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Sem suporte no Windows Installer 4,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4307422c71976057948759078dc321e38dc543b7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105766388"
---
# <a name="not-supported-in-windows-installer-40"></a>Sem suporte no Windows Installer 4,0

O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 4,0 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso tenha suporte. Consulte a documentação principal para determinar qual versão de Windows Installer é necessária para um recurso específico. Para obter informações sobre outras versões do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 4,0 está disponível para o Microsoft Windows Server 2008 e o Windows Vista. Para obter uma lista completa de todas as versões e redistribuíveis do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Installer 4,0 e versões anteriores.

[Funções do instalador](installer-functions.md)

-   [**MsiBeginTransaction**](/windows/desktop/api/Msi/nf-msi-msibegintransactiona)
-   [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction)
-   [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction)

[Propriedades](properties.md)

-   [**MSIDISABLEEEUI**](msidisableeeui.md)
-   [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)

[Tabelas de banco de dados](database-tables.md)

-   [Tabela MsiEmbeddedChainer](msiembeddedchainer-table.md)
-   [Tabela MsiEmbeddedUI](msiembeddedui-table.md)
-   [Tabela MsiPackageCertificate](msipackagecertificate-table.md)
-   [Tabela de componentes](component-table.md)
- **msidbComponentAttributesUninstallOnSupersedence**  
    **msidbComponentAttributesShared**  
    
-   [CustomAction](customaction-table.md) Coluna Extended  
    

[Opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md)



[MsiTransformView\<PatchGUID\>](msitransformview.md)  

**msidbCustomActionTypePatchUninstall**  


[Política do sistema](system-policy.md)

-   [DisableSharedComponent](disablesharedcomponent.md)
-   [MsiDisableEmbeddedUI](msidisableembeddedui.md)

Protótipos de função de retorno de chamada

-   *EmbeddedUIHandler*
-   *InitializeEmbeddedUI*
-   *ShutdownEmbeddedUI*

[Avaliadores de consistência internos-ICEs](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) verifica se nenhum componente tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** .

## <a name="notes"></a>Observações

Windows Installer 4,0 não pode executar [várias instalações de pacote](multiple-package-installations.md) usando o [*processamento de transações*](t-gly.md).

Usando o Windows Installer 4,0 ou versões anteriores do instalador, pequenas atualizações e pequenos upgrades podem falhar ao usar a política [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) ou a propriedade [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) porque a atualização remove um componente.

Uma interface do usuário personalizada não pode ser inserida no pacote de Windows Installer usando o método descrito em [usando uma interface do usuário inserida](using-an-embedded-ui.md).

 

 



