---
description: O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer&\# 160; 2.0 e versões anteriores.
ms.assetid: 850b598a-338e-4f84-8336-01e962256a08
title: Sem suporte no Windows Installer 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ee09133af9ef611a93c2511d7b130b2175561b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837200"
---
# <a name="not-supported-in-windows-installer-20"></a>Sem suporte no Windows Installer 2,0

O Windows Installer funções, tabelas e propriedades listadas nesta página não têm suporte do Windows Installer 2,0 e versões anteriores. A ausência de um recurso dessa lista não garante que o recurso tenha suporte. Consulte a documentação principal para determinar qual versão de Windows Installer é necessária para um recurso específico. Para obter informações sobre outras versões do Windows Installer, consulte [o que há de novo no Windows Installer](what-s-new-in-windows-installer.md).

O Windows Installer 2,0 pode ser executado no Microsoft Windows 2000, no Microsoft Windows XP ou no Windows Server 2003. Para obter uma lista de todas as versões do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

Os recursos a seguir não têm suporte no Windows Installer 2,0 e versões anteriores.

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

[Estruturas de Windows Installer](installer-structures.md)

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
    -   [**Installer. PatchesEx**](installer-patchesex.md)

-   Métodos do [ **objeto instalador**](installer-object.md)

    -   [**Installer. ApplyMultiplePatches**](installer-applymultiplepatches.md)
    -   [**Installer. ApplyPatch**](installer-applypatch.md)
    -   [**Installer. RemovePatches**](installer-removepatches.md)
    -   [**Installer. ExtractPatchXMLData**](installer-extractpatchxmldata.md)

Os recursos a seguir também não têm suporte no Windows Installer versão 2.0.2600. Windows Installer versão 2.0.2600 foi lançada com o Windows XP e o Windows 2000 Server. Os recursos estão disponíveis a partir do Windows Installer versão 2.0.3790 lançada com o Windows Server 2003. Para obter uma lista de todas as versões do Windows Installer, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

[Funções do instalador](installer-functions.md)

-   [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)
    -   instância de MSIADVERTISEOPTIONS \_
-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)

[Interface de automação](automation-interface.md)

-   Métodos do [ **objeto instalador**](installer-object.md)

    -   [**Installer. ApplyPatch**](installer-applypatch.md)
    -   [**Installer. ProductInfo**](installer-productinfo.md)

[Propriedades](properties.md)

-   [**MSINEWINSTANCE**](msinewinstance.md)
-   [**MSIINSTANCEGUID**](msiinstanceguid.md)
-   [**MsiNTSuiteWebServer**](msintsuitewebserver.md)

[Opções de execução de In-Script de ação personalizada](custom-action-in-script-execution-options.md)

-   [**msidbCustomActionTypeTSAware**](custom-action-in-script-execution-options.md)

[Códigos de Erro](error-codes.md)

-   [ERRO ao \_ instalar \_ remoto \_ proibido](error-codes.md)

[Políticas do computador](machine-policies.md)

-   [DisableMSI](disablemsi.md)
-   [Política de TransformsSecure](transformssecure-policy.md)

[Opções de linha de comando](command-line-options.md)

-   [/c](command-line-options.md)
-   [opção](command-line-options.md)
-   [/Lx](command-line-options.md)

[Atributos de controle](control-attributes.md)

-   **ImageHandle** foi removido

## <a name="notes"></a>Observações

As [Opções de Command-Line do instalador padrão](standard-installer-command-line-options.md) não são suportadas pelo Windows Installer 2,0. Em vez disso, use as [Opções de linha de comando](command-line-options.md)Windows Installer.

Quando Windows Installer 2,0 instala um pacote de patch, ele ignora as informações nas tabelas [MsiPatchSequence](msipatchsequence-table.md) ou [MsiPatchMetaData](msipatchmetadata-table.md) . As versões posteriores do Windows Installer podem usar as informações nessas tabelas para melhorar o sequenciamento, a remoção e a otimização de patches. Para obter informações sobre a funcionalidade de aplicação de patch aprimorada no Windows Installer, consulte [aplicação de patches](patching.md).

Windows Installer 2,0 não oferece suporte a [patches desinstaláveis](uninstallable-patches.md) e o único método para remover patches específicos de um aplicativo é desinstalar todo o aplicativo com patch e reinstalá-lo sem reaplicar os patches que estão sendo removidos.

Windows Installer 2,0 não oferece suporte ao sequenciamento de patches e instala patches na ordem em que são fornecidos ao sistema ao [instalar vários patches](installing-multiple-patches.md).

Windows Installer 2,0 não oferece suporte ao uso de [aplicação de patch de UAC (controle de conta de usuário)](user-account-control--uac--patching.md) para habilitar patches assinados digitalmente que podem ser aplicados por usuários não administradores.

Windows Installer 2,0 não oferece suporte à [otimização de patch](patch-optimization.md). A aplicação de patch pode levar muito mais tempo do que as versões mais recentes do Windows Installer que atualizam apenas os arquivos afetados pelo patch.

Windows Installer 2,0 não oferece suporte ao [uso de Windows Installer para inventariar produtos e patches](inventory-products-and-patches-.md).

Windows Installer 2,0 não oferece suporte à recuperação e à modificação de informações da lista de origem para aplicativos Windows Installer e patches instalados no sistema para todos os usuários. As versões posteriores do Windows Installer permitem que os administradores gerenciem listas de origem e propriedades da lista de origem para fontes de rede, URL e mídia. As versões posteriores permitem que os administradores gerenciem listas de origem de um processo externo. Para obter mais informações, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).

Windows Installer 2,0 não oferece suporte à instalação de várias instâncias de produtos ou patches sem um pacote de instalação separado para cada instância. Versões mais recentes do Windows Installer podem instalar várias instâncias de um produto usando transformações de código do produto e um pacote. msi ou um patch. Para obter informações [, consulte Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).

A partir do Windows XP com Service Pack 2 (SP2), Windows Installer pode usar os protocolos HTTP, HTTPS e FILE. O instalador não dá suporte aos protocolos FTP e GOPHER.

 

 



