---
description: A tabela UpgradedImages contém informações sobre as imagens atualizadas do produto.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Tabela UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297440"
---
# <a name="upgradedimages-table-patchwizdll"></a>Tabela UpgradedImages (Patchwiz.dll)

A tabela UpgradedImages contém informações sobre as imagens atualizadas do produto. A imagem atualizada deve ser uma imagem de instalação totalmente descompactada da versão mais recente do produto, por exemplo, uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM. Um pacote de patch Windows Installer atualiza uma imagem de destino em uma imagem atualizada. A tabela UpgradedImages é necessária no banco de dados de criação de patch (arquivo. PCP) e é usada pelo [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

Uma tabela UpgradedImages contendo pelo menos um registro é necessária em cada banco de dados de criação de patch (arquivo. PCP). Essa tabela é usada pelo [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).

A tabela UpgradedImages tem as colunas a seguir.



| Coluna       | Tipo | Chave | Nullable |
|--------------|------|-----|----------|
| Atualizado     | text | S   | N        |
| MsiPath      | text |     | N        |
| PatchMsiPath | text |     | S        |
| SymbolPaths  | text |     | S        |
| Família       | text |     | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram
</dt> <dd>

O campo atualizado é um identificador arbitrário para conectar as imagens de destino com uma imagem atualizada do produto.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Este campo especifica o caminho completo, incluindo o nome do arquivo, para o local do arquivo. msi para a imagem atualizada. Este é o local dos arquivos de origem para a imagem atualizada.

</dd> <dt>

<span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath
</dt> <dd>

O patchMsiPath opcional aponta para uma cópia modificada do banco de dados de instalação atualizado que contém a criação adicional específica do processo de instalação do patch. Por exemplo, caixas de diálogo adicionais ou ações personalizadas condicionadas na propriedade [**patch**](patch.md) .

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Uma lista delimitada por ponto e vírgula de pastas que devem ser pesquisadas para arquivos de símbolo que podem ser usados para otimizar a geração do patch binário. Observe que os subdiretórios das pastas especificadas neste campo não são pesquisados. Um patch binário otimizado pode ser menor. Visual C++ deve ser instalado no computador que gera o patch e usado para criar os arquivos de símbolo. Esse campo é opcional e o instalador cria um patch binário, mesmo se nenhum arquivo de símbolo for especificado ou se os arquivos de símbolo ficarem indisponíveis para Patchwiz.dll.

</dd> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Parentes
</dt> <dd>

Chave estrangeira na [tabela ImageFamilies](imagefamilies-table-patchwiz-dll-.md). Cada imagem atualizada deve pertencer a apenas uma família.

</dd> </dl>

## <a name="remarks"></a>Comentários

Embora cada imagem atualizada possa ser agrupada em uma família de imagens separada, o agrupamento de imagens atualizadas que compartilham arquivos pode tornar o. msp menor.

Esta tabela aceita variáveis de ambiente como caminhos que começam com a versão 4,0 de Patchwiz.dll.

 

 



