---
description: Para gerar um pacote de patch, é recomendável que você use uma ferramenta de criação de patch, como Msimsp.exe e Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172009"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Para gerar um pacote de patch, é recomendável que você use uma ferramenta de criação de patch, como [Msimsp.exe](msimsp-exe.md) e Patchwiz.dll. Patchwiz.dll versão 4,0 é compatível com pacotes e patches que foram criados usando versões anteriores do Patchwiz.dll. A ferramenta de Patchwiz.dll só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Patchwiz.dll versão 4,0 tem uma nova função, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), que estende a funcionalidade de [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md). Essas funções usam um arquivo de propriedades de criação de patch (arquivo. PCP) e geram um [pacote de patch](patch-packages.md)do instalador.

O arquivo. PCP é um arquivo de banco de dados binário com o mesmo formato que um banco de dados Windows Installer (arquivo. msi), mas com um esquema de banco de dados diferente. Portanto, um arquivo. PCP pode ser criado usando as mesmas ferramentas usadas para um banco de dados do instalador.

Você pode criar um arquivo. PCP usando um editor de tabela, como [Orca.exe](orca-exe.md) para inserir informações no banco de dados. PCP em branco fornecido com o SDK do Windows Installer, template. PCP. Para obter mais informações, consulte [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).

As tabelas de banco de dados a seguir são necessárias em todos os arquivos. PCP:

-   [Tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Tabela ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Tabela TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

As seguintes tabelas de banco de dados são opcionais:

-   [\_Tabela UpgradedFiles OptionalData (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabela FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [\_Tabela TargetFiles OptionalData (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabela ExternalFiles (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Tabela UpgradedFilesToIgnore (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

A tabela a seguir é necessária em arquivos. PCP que têm um MinimumRequiredMsiVersion igual a 300 na tabela de [Propriedades](properties-table-patchwiz-dll-.md) .

-   [Tabela PatchMetadata (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> A tabela será opcional se MinimumRequiredMsiVersion não for igual a 300.

 

A versão do Patchwiz.dll lançada com Windows Installer 3,0 pode gerar automaticamente informações de sequenciamento de patch e adicioná-las à [tabela MsiPatchSequence](msipatchsequence-table.md) de um novo patch. A [tabela PatchSequence](patchsequence-table--patchwiz-dll-.md) pode ser usada para adicionar manualmente informações de sequenciamento de patch à tabela MsiPatchSequence. Para obter mais informações, consulte [gerando informações de sequência de patch](generating-patch-sequence-information---patchwiz-dll-.md).

A partir do Patchwiz.dll versão 2,0, você pode aumentar a velocidade da criação de patch subsequente usando o [cache de informações de patch (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md).

Usar símbolos públicos para seus binários de imagem de destino e de atualização pode reduzir tamanhos de patch binários por aproximadamente uma metade. Para obter mais informações, consulte [usando símbolos para reduzir o tamanho do patch binário](using-symbols-to-reduce-binary-patch-size.md).

É possível especificar que determinadas regiões do arquivo de destino sejam substituídas durante a aplicação de patch e que as informações nessas regiões sejam retidas. Para obter mais informações, consulte [aplicação de patch nas regiões selecionadas de um arquivo](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



