---
description: A tabela TargetImages contém informações sobre as imagens de destino do produto. Um Windows patch do instalador atualiza uma imagem de destino em uma imagem atualizada.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabela TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec35a9090f89e93e807cda9429ae48d8cc28d175acc4c83e97150e3a98ce5fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893586"
---
# <a name="targetimages-table-patchwizdll"></a>Tabela TargetImages (Patchwiz.dll)

A tabela TargetImages contém informações sobre as imagens de destino do produto. Um Windows patch do instalador atualiza uma imagem de destino em uma imagem atualizada.

Uma tabela TargetImages que contém pelo menos um registro é necessária em cada banco de dados de criação de patch (arquivo .pcp). Essa tabela é usada pela [função UiCreatePatchPackage.](uicreatepatchpackage-patchwiz-dll-.md)

A tabela TargetImages tem as seguintes colunas.



| Coluna                | Tipo    | Chave | Nullable |
|-----------------------|---------|-----|----------|
| Destino                | texto    | Y   | N        |
| MsiPath               | texto    |     | N        |
| SymbolPaths           | texto    |     | Y        |
| Atualizado              | texto    |     | N        |
| Ordem                 | Número inteiro |     | N        |
| ProductValidateFlags  | texto    |     | Y        |
| IgnoreMissingSrcFiles | Número inteiro |     | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo
</dt> <dd>

Identificador de uma imagem de destino. O pacote de patch atualiza a imagem de destino especificada nesta coluna para a imagem atualizada especificada na coluna Atualizado. Há uma ou mais imagens de destino para cada imagem atualizada. A imagem de destino deve ser uma imagem de configuração totalmente descompactada do produto, como uma imagem administrativa ou uma imagem de instalação descompactada em um CD-ROM. Observe que a [função UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) não gera patches binários para arquivos em gabinetes. O valor nesse campo é usado com o valor no campo Atualizado para gerar os nomes das transformaçãos que o instalador adiciona ao pacote de patch.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Esse campo especifica o caminho completo, incluindo o nome do arquivo, para o local do arquivo .msi para a imagem de destino. Esse é o local dos arquivos de origem para a imagem de destino.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Uma lista delimitada por ponto e vírgula de pastas que devem ser pesquisadas para arquivos de símbolo que podem ser usados para otimizar a geração do patch binário. Observe que os subdireários de pastas especificados neste campo não são pesquisados. Um patch binário otimizado pode ser menor. Microsoft Visual C++ deve ser instalado no computador que está gerando o patch e usado para criar os arquivos de símbolo. Esse campo é opcional e o instalador cria um patch binário, mesmo se nenhum arquivo de símbolo for especificado ou se os arquivos de símbolo se tornarem indisponíveis para Patchwiz.dll.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Atualizado
</dt> <dd>

Chave estrangeira para a coluna Atualizado da [tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md). A [função UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) ignora qualquer imagem atualizada que não seja referenciada por pelo menos um registro da tabela TargetImages.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordem
</dt> <dd>

Ordem relativa da imagem de destino. Como vários destinos podem ser corrigidas em uma imagem atualizada, o campo Ordem fornece um meio para sequenciar as transformaçãos na lista de transformaçãos de patch. Normalmente, a ordem é da imagem mais antiga para a mais recente.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

O campo ProductValidateFlags é usado para especificar a verificação de produtos para evitar a aplicação de transformação irrelevantes. O valor inserido nesse campo deve ser um inteiro hexadiom de 8 dígitos e um dos valores válidos para o parâmetro *iValidation* da [**função MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) O valor padrão é 0x00000922 que é igual a **MSITRANSFORM \_ VALIDATE \_ UPDATEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ UPGRADECODE**  +  **MSITRANSFORM \_ VALIDATE \_ PRODUCT**.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

Se esse campo for definido como um valor diferente de zero, os arquivos ausentes da imagem de destino serão ignorados pelo instalador e deixados inalterados durante a adoção de patch. Isso permite que os patches sejam feitos sem a necessidade de toda a imagem; somente os arquivos alterados do produto e o arquivo .msi são necessários. Isso pode reduzir o tempo necessário para gerar o patch.

> [!Note]  
> Não use o valor IgnoreMissingSrcFiles com TrustMsi definido como 1 na [Tabela de Propriedades](properties-table-patchwiz-dll-.md).

 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela aceita variáveis de ambiente como caminhos começando com a versão 4.0 do Patchwiz.dll.

 

 



