---
description: o Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer&\# 160; 2.0 e versões anteriores.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: sem suporte no Windows Installer 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d244dc962e65bb017dbd5fb56c7fda644b46524df7890ede7b71bf0bdf8ad66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074856"
---
# <a name="not-supported-in-windows-installer-20"></a>sem suporte no Windows Installer 2,0

o Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 2,0 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso tenha suporte. consulte a documentação principal para determinar qual versão de Windows Installer é necessária para um recurso específico. para obter informações sobre outras versões do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).

Windows o instalador 2,0 pode ser executado no microsoft Windows 2000, no microsoft Windows XP ou no Windows Server 2003. para obter uma lista de todas as versões do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

os recursos a seguir não têm suporte no Windows Installer 2,0 e versões anteriores.

[Funções do instalador](installer-functions.md)

-   [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
-   [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
-   [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
-   [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
-   [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
-   [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
-   [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa)
-   [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
-   [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
-   [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
-   [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
-   [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
-   [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
-   [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
-   [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
-   [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa)
-   [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
-   [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
-   [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
-   [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
-   [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

[Windows Estruturas do instalador](installer-structures.md)

-   [**MSIPATCHSEQUENCEINFO**](/windows/win32/api/msi/ns-msi-msipatchsequenceinfoa)

[Tabelas de banco de dados](database-tables.md)

-   [MsiPatchCertificate](msipatchcertificate-table.md)
-   [MsiPatchSequence](msipatchsequence-table.md)
-   [MsiPatchMetadata](msipatchmetadata-table.md)

[Propriedades](properties.md)

-   [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
-   [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)
-   [**MSIPATCHREMOVE**](msipatchremove.md)
-   [**MsiPatchRemovalList**](msipatchremovallist.md)
-   [**MsiUISourceResOnly**](msiuisourceresonly.md)
-   [**MsiUIHideCancel**](msiuihidecancel.md)
-   [**MsiUIProgressOnly**](msiuiprogressonly.md)

[Política do sistema](system-policy.md)

-   [DisableLUAPatching](disableluapatching.md)
-   [DisablePatchUninstall](disablepatchuninstall.md)
-   [DisableFlyWeightPatching](disableflyweightpatching.md)
-   [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md)
-   [MaxPatchCacheSize](maxpatchcachesize.md)

[Códigos de Erro](error-codes.md)

-   remoção de patch de erro \_ \_ \_ sem suporte
-   ERRO \_ de \_ patch desconhecido
-   PATCH de erro \_ \_ sem \_ sequência
-   remoção de patch de erro não \_ \_ \_ permitida
-   ERRO \_ \_ XML de patch inválido \_
-   ERRO \_ de \_ \_ produto anunciado gerenciado por patch \_

Modos de log

-   [**INSTALLLOGMODE \_ LOGONLYONERROR**](/windows/desktop/api/Msi/nf-msi-msienableloga)

[Interface de automação](automation-interface.md)

-   Propriedades do [ **objeto Product**](product-object.md)

    -   [**Product. UserId**](product-usersid.md)
    -   [**Produto. fontes**](product-sources.md)
    -   [**Product. MediaDisks**](product-mediadisks.md)
    -   [**Produto. Featurestate**](product-featurestate.md)
    -   [**Product. Context**](product-context.md)
    -   [**Produto. InstallProperty**](product-installproperty.md)
    -   [**Product. ProductCode**](product-productcode.md)
    -   [**Product. Componentstate**](product-componentstate.md)
    -   [**Produto. estado**](product-state.md)
    -   [**Product. SourceListInfo**](product-sourcelistinfo.md)

-   Métodos do [ **objeto Product**](product-object.md)

    -   [**Product. SourceListForceResolution**](product-sourcelistforceresolution.md)
    -   [**Product. SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)
    -   [**Product. SourceListClearAll**](product-sourcelistclearall.md)
    -   [**Product. SourceListClearSource**](product-sourcelistclearsource.md)
    -   [**Product. SourceListAddSource**](product-sourcelistaddsource.md)
    -   [**Product. SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)

-   Propriedades do [ **objeto patch**](patch-object.md)

    -   [**Patch. UserId**](patch-usersid.md)
    -   [**Patch. State**](patch-state.md)
    -   [**Patch. Sources**](patch-sources.md)
    -   [**Patch. SourceListInfo**](patch-sourcelistinfo.md)
    -   [**Patch. ProductCode**](patch-productcode.md)
    -   [**Patch. Patchproperty**](patch-patchproperty.md)
    -   [**Patch. PatchCode**](patch-patchcode.md)
    -   [**Patch. MediaDisks**](patch-mediadisks.md)
    -   [**Patch. Context**](patch-context.md)

-   Métodos do [ **objeto patch**](patch-object.md)

    -   [**Patch. SourceListForceResolution**](patch-sourcelistforceresolution.md)
    -   [**Patch. SourceListClearAll**](patch-sourcelistclearall.md)
    -   [**Patch. SourceListClearSource**](patch-sourcelistclearsource.md)
    -   [**Patch. SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)
    -   [**Patch. SourceListAddSource**](patch-sourcelistaddsource.md)
    -   [**Patch. SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)

-   Propriedades do [ **objeto instalador**](installer-object.md)

    -   [**Installer. ProductsEx**](installer-productsex.md)
    -   [**Installer. ProductInfo**](installer-productinfo.md)
    -   [**Installer.PatchesEx**](installer-patchesex.md)

-   Métodos do [ **objeto installer**](installer-object.md)

    -   [**Installer.ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.RemovePatches**](installer-removepatches.md)
    -   [**Installer.ExtractPatchXMLData**](installer-extractpatchxmldata.md)

Os recursos a seguir também não têm suporte no Windows Installer versão 2.0.2600. Windows O instalador versão 2.0.2600 foi lançado com Windows XP e Windows 2000 Server. Os recursos estão disponíveis a partir do Windows Installer versão 2.0.3790 lançado com o Windows Server 2003. Para ver uma lista de todas as Windows do Instalador, consulte Versões lançadas [do Windows Installer](released-versions-of-windows-installer.md).

[Funções do instalador](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   INSTÂNCIA MSIADVERTISEOPTIONS \_
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Interface de Automação](automation-interface.md)

-   Métodos do [ **objeto installer**](installer-object.md)

    -   [**Installer.ApplyPatch**](installer-applypatch.md)
    -   [**Installer.ProductInfo**](installer-productinfo.md)

[Propriedades](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Opções de execução In-Script ação personalizada](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Códigos de Erro](error-codes.md)

-   [ERRO \_ AO INSTALAR \_ \_ REMOTAMENTE PROIBIDO](error-codes.md)

[Políticas de computador](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [TransformsSeure policy](transformssecure-policy.md)

[Opções de linha de comando](command-line-options.md)

-   [/c](command-line-options.md)
-   [/n](command-line-options.md)
-   [/Lx](command-line-options.md)

[Atributos de controle](control-attributes.md)

-   **ImageHandle** foi removido

## <a name="notes"></a>Observações

Não há suporte para [Command-Line standard Installer](standard-installer-command-line-options.md) no Windows Installer 2.0. Em vez disso, use Windows opções de linha de comando [do instalador de dados.](command-line-options.md)

Quando Windows Installer 2.0 instala um pacote de patch, ele ignora informações nas tabelas [MsiPatchSequence](msipatchsequence-table.md) ou [MsiPatchMetadata.](msipatchmetadata-table.md) Versões posteriores do Windows Instalador podem usar as informações nessas tabelas para melhorar o sequenciamento, a remoção e a otimização de patch. Para obter informações sobre a funcionalidade de aprimorada de adoção Windows Instalador, consulte [Patching](patching.md).

Windows O Instalador 2.0 não dá suporte a [Patches Desinstaláveis](uninstallable-patches.md) e o único método para remover patches específicos de um aplicativo é desinstalar todo o aplicativo com patch e reinstalar sem reaplicação de patches que estão sendo removidos.

Windows O Instalador 2.0 não dá suporte ao sequenciamento de patch e instala patches na ordem em que eles são fornecidos ao sistema ao instalar [vários patches](installing-multiple-patches.md).

Windows O Instalador 2.0 não dá suporte ao uso da Aplicação de Patch do [UAC (Controle](user-account-control--uac--patching.md) de Conta de Usuário) para habilitar patches assinados digitalmente que podem ser aplicados por usuários não administradores.

Windows O Instalador 2.0 não dá suporte à [Otimização de Patch.](patch-optimization.md) A adoção de patch pode levar muito mais tempo do que com as versões Windows Instalador posteriores que atualiza apenas os arquivos afetados pelo patch.

Windows O Instalador 2.0 não dá suporte ao [Uso Windows Instalador para Produtos de](inventory-products-and-patches-.md)Inventário e Patches .

Windows O Instalador 2.0 não dá suporte à recuperação e modificação das informações da lista de origem para aplicativos e patches do instalador do Windows instalados no sistema para todos os usuários. Versões posteriores do Windows Instalador permitem que os administradores gerenciem listas de origem e propriedades da lista de origem para fontes de rede, URL e mídia. Versões posteriores permitem que os administradores gerenciem listas de origem de um processo externo. Para obter mais informações, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).

Windows O Instalador 2.0 não dá suporte à instalação de várias instâncias de produtos ou patches sem um pacote de instalação separado para cada instância. Posteriormente Windows versões do Instalador podem instalar várias instâncias de um produto usando as transformaçãos de código do produto e um .msi pacote ou um patch. Para obter [informações, consulte Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).

A partir do Windows XP com o SERVICE Pack 2 (SP2), o Windows Installer pode usar os protocolos HTTP, HTTPS e FILE. O instalador não dá suporte aos protocolos FTP e GOPHER.

 

 



