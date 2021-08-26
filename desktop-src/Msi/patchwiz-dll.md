---
description: Para gerar um pacote de patch, é recomendável usar uma ferramenta de criação de patch, como Msimsp.exe e Patchwiz.dll.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de7a099a95eb6b42341b7f440f15fadb42e6a5ea8bbf69ff4d61b1fcaa28d21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129166"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Para gerar um pacote de patch, é recomendável usar uma ferramenta de criação de patch, [ como ](msimsp-exe.md)Msimsp.exee Patchwiz.dll. Patchwiz.dll versão 4.0 é compatível com pacotes e patches que foram autorados usando versões anteriores do Patchwiz.dll. A Patchwiz.dll do Patchwiz.dll está disponível apenas nos componentes [do SDK do Windows para desenvolvedores Windows instalador.](platform-sdk-components-for-windows-installer-developers.md)

Patchwiz.dll versão 4.0 tem uma nova função, [UiCreatePatchPackageEx (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), que estende a funcionalidade [de UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md). Essas funções levam um arquivo de propriedades de criação de patch (arquivo .pcp) e geram um Pacote de [Patch do instalador.](patch-packages.md)

O arquivo .pcp é um arquivo de banco de dados binário com o mesmo formato que um banco de dados Windows Installer (arquivo .msi), mas com um esquema de banco de dados diferente. Portanto, um arquivo .pcp pode ser autorado usando as mesmas ferramentas usadas para um banco de dados do instalador.

Você pode criar um arquivo .pcp usando um editor de tabelas como [Orca.exe](orca-exe.md) para inserir informações no banco de dados .pcp em branco fornecido com o SDK do Instalador do Windows, Template.pcp. Para obter mais informações, consulte [Um pequeno exemplo de a](a-small-update-patching-example.md)patch de atualização .

As tabelas de banco de dados a seguir são necessárias em cada arquivo .pcp:

-   [Tabela de propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Tabela ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [Tabela TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

As tabelas de banco de dados a seguir são opcionais:

-   [Tabela UpgradedFiles \_ OptionalData (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabela FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [Tabela TargetFiles \_ OptionalData (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Tabela ExternalFiles (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Tabela UpgradedFilesToIgnore (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

A tabela a seguir é necessária em arquivos .pcp que têm um MinimumRequiredMsiVersion igual a 300 na [tabela](properties-table-patchwiz-dll-.md) Propriedades.

-   [Tabela PatchMetadata (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> A tabela será opcional se MinimumRequiredMsiVersion não for igual a 300.

 

A versão do Patchwiz.dll lançada com o Windows Installer 3.0 pode gerar automaticamente informações de sequenciamento de patch e adicioná-la à Tabela [MsiPatchSequence](msipatchsequence-table.md) de um novo patch. A [Tabela PatchSequence pode](patchsequence-table--patchwiz-dll-.md) ser usada para adicionar manualmente informações de sequenciamento de patch à tabela MsiPatchSequence. Para obter mais informações, consulte [Gerando informações de sequência de patch](generating-patch-sequence-information---patchwiz-dll-.md).

A partir Patchwiz.dll versão 2.0 Caching, você pode aumentar a velocidade da criação subsequente de patch usando o Patchwiz.dll [(Informações de Patch).](patch-information-caching-patchwiz-dll-.md)

O uso de símbolos públicos para os binários de imagem de destino e atualização pode reduzir os tamanhos de patch binários em aproximadamente metade. Para obter mais informações, consulte [Using Symbols to Reduce Binary Patch Size](using-symbols-to-reduce-binary-patch-size.md).

Você pode especificar que determinadas regiões do arquivo de destino sejam preservadas de serem substituídas durante a adoção de patch e que as informações nessas regiões sejam mantidas. Para obter mais informações, consulte [Patching Selected Regions of a File](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões, ferramentas e redistribuíveis lançados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



