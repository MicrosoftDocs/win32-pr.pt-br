---
description: A tabela TargetImages contém informações sobre as imagens de destino do produto. Um pacote de patch Windows Installer atualiza uma imagem de destino em uma imagem atualizada.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabela TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837105"
---
# <a name="targetimages-table-patchwizdll"></a>Tabela TargetImages (Patchwiz.dll)

A tabela TargetImages contém informações sobre as imagens de destino do produto. Um pacote de patch Windows Installer atualiza uma imagem de destino em uma imagem atualizada.

Uma tabela TargetImages contendo pelo menos um registro é necessária em cada banco de dados de criação de patch (arquivo. PCP). Essa tabela é usada pela função [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) .

A tabela TargetImages tem as colunas a seguir.



| Coluna                | Tipo    | Chave | Nullable |
|-----------------------|---------|-----|----------|
| Destino                | text    | S   | N        |
| MsiPath               | text    |     | N        |
| SymbolPaths           | text    |     | S        |
| Atualizado              | text    |     | N        |
| Ordem                 | Número inteiro |     | N        |
| ProductValidateFlags  | text    |     | S        |
| IgnoreMissingSrcFiles | Número inteiro |     | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo
</dt> <dd>

Identificador para uma imagem de destino. O pacote de patch atualiza a imagem de destino especificada nesta coluna para a imagem atualizada especificada na coluna atualizado. Há uma ou mais imagens de destino para cada imagem atualizada. A imagem de destino deve ser uma imagem de instalação totalmente descompactada do produto, como uma imagem administrativa ou uma imagem de instalação descompactada em um CD-ROM. Observe que a função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) não gera patches binários para arquivos em gabinetes. O valor nesse campo é usado com o valor no campo atualizado para gerar os nomes das transformações que o instalador adiciona ao pacote de patch.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Este campo especifica o caminho completo, incluindo o nome do arquivo, para o local do arquivo. msi para a imagem de destino. Este é o local dos arquivos de origem para a imagem de destino.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Uma lista delimitada por ponto e vírgula de pastas que devem ser pesquisadas para arquivos de símbolo que podem ser usados para otimizar a geração do patch binário. Observe que os subdiretórios das pastas especificadas neste campo não são pesquisados. Um patch binário otimizado pode ser menor. Microsoft Visual C++ deve ser instalado no computador que gera o patch e usado para criar os arquivos de símbolo. Esse campo é opcional e o instalador cria um patch binário, mesmo se nenhum arquivo de símbolo for especificado ou se os arquivos de símbolo ficarem indisponíveis para Patchwiz.dll.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram
</dt> <dd>

Chave estrangeira para a coluna atualizada da [tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md). A função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignora qualquer imagem atualizada que não seja referenciada por pelo menos um registro da tabela TargetImages.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene
</dt> <dd>

Ordem relativa da imagem de destino. Como vários destinos podem ser corrigidos para uma imagem atualizada, o campo ordem fornece um meio de sequenciar as transformações na lista de transformações de patch. Normalmente, o pedido é da imagem mais antiga para a mais nova.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

O campo ProductValidateFlags é usado para especificar a verificação do produto para evitar a aplicação de transformações irrelevantes. O valor inserido nesse campo deve ser um inteiro hexadecimal de 8 dígitos e um dos valores válidos para o parâmetro *iValidation* da função [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) . O valor padrão é 0x00000922, que é igual a **MSITRANSFORM \_ validar \_ UPDATEVERSION**  +  **MSITRANSFORM \_ validar \_ NEWEQUALBASEVERSION** MSITRANSFORM  +  **\_ validar \_ UPGRADECODE**  +  **MSITRANSFORM \_ validar \_ produto**.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

Se esse campo for definido como um valor diferente de zero, os arquivos ausentes da imagem de destino serão ignorados pelo instalador e deixados inalterados durante a aplicação de patch. Isso permite que os patches sejam feitos sem a necessidade de toda a imagem; somente os arquivos alterados do produto e do arquivo. msi são necessários. Isso pode reduzir o tempo necessário para gerar o patch.

> [!Note]  
> Não use o valor IgnoreMissingSrcFiles com TrustMsi definido como 1 na [tabela Propriedades](properties-table-patchwiz-dll-.md).

 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela aceita variáveis de ambiente como caminhos que começam com a versão 4,0 de Patchwiz.dll.

 

 



