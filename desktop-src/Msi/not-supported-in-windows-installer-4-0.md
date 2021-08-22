---
description: As funções, tabelas e propriedades do instalador Windows Windows listadas nesta página não têm suporte do Windows Installer&\# 160;4.0 e versões anteriores.
ms.assetid: 7256b759-3fb5-4195-b0e4-a1631327ebb7
title: Sem suporte no Windows 4.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444040fca716b6bd64c8598d2d2e36013fe19cc62971483507756a66f3e961bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558796"
---
# <a name="not-supported-in-windows-installer-40"></a>Sem suporte no Windows 4.0

As Windows, tabelas e propriedades listadas nesta página não são suportadas pelo Windows Installer 4.0 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso seja suportado. Consulte a documentação principal para determinar qual Windows do Instalador é necessária para um recurso específico. Para obter informações sobre Windows versões do Instalador, consulte [Novidades no Windows Installer](what-s-new-in-windows-installer.md).

Windows O Instalador 4.0 está disponível para Microsoft Windows Server 2008 e Windows Vista. Para ver uma lista completa de todas as versões Windows instalador e redistribuíveis, consulte Versões lançadas [do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Installer 4.0 e versões anteriores.

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
    
-   [CustomAction](customaction-table.md) Coluna ExtendedType  
    

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

[Avaliadores de consistência interna – ICEs](internal-consistency-evaluators-ices.md)

-   [ICE92](ice92.md) verifica se nenhum componente tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence.**

## <a name="notes"></a>Observações

Windows O Instalador 4.0 não pode executar [várias instalações de pacote](multiple-package-installations.md) usando o processamento de [*transações*](t-gly.md).

Usando o Windows Installer 4.0 ou versões anteriores do instalador, pequenas atualizações e atualizações secundárias podem falhar ao usar a política [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) ou a [**propriedade MSFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) porque a atualização remove um componente.

Uma interface do usuário personalizada não pode ser inserida no pacote Windows Instalador usando o método descrito em [Usando uma interface do usuário inserida.](using-an-embedded-ui.md)

 

 



