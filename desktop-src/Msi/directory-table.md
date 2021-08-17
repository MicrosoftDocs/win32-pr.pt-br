---
description: A tabela Diretório especifica o layout do diretório para o produto. Cada linha da tabela indica um diretório na origem e no destino.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabela de diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19e9b5994062ac55564799854fc36016fc6ddb9887bc36aa9a94652ef31aeb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947340"
---
# <a name="directory-table"></a>Tabela de diretórios

A tabela Diretório especifica o layout do diretório para o produto. Cada linha da tabela indica um diretório na origem e no destino.

A tabela Diretório tem as seguintes colunas.



| Coluna            | Tipo                         | Chave | Nullable |
|-------------------|------------------------------|-----|----------|
| Diretório         | [Identificador](identifier.md) | Y   | N        |
| Pai do \_ Diretório | [Identificador](identifier.md) | N   | Y        |
| Defaultdir        | [Defaultdir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Diretório
</dt> <dd>

A coluna Diretório contém um identificador exclusivo para um diretório ou caminho de diretório. Essa coluna pode conter o nome de uma propriedade definida como o caminho completo de um diretório de destino. Se essa coluna contiver uma propriedade , o diretório de destino será o nome especificado na coluna DefaultDir e o diretório pai especificado na coluna \_ Pai do Diretório.

O diretório de origem sempre recebe o nome especificado na coluna DefaultDir e assume o diretório pai especificado na coluna \_ Pai do Diretório.

Se a coluna Pai do Diretório for nula ou igual ao valor da coluna Diretório, a coluna \_ Diretório representará um diretório de destino raiz. Somente um diretório raiz pode ser especificado na tabela Diretório.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Pai do \_ Diretório
</dt> <dd>

Essa coluna é uma referência ao diretório pai do diretório. Um registro que tem uma coluna Pai do Diretório igual a null ou igual à \_ coluna Directory representa um diretório raiz. O caminho completo do diretório pai é resolvido por referência na coluna Pai do Diretório é uma \_ chave externa na coluna Diretório. Por exemplo, se uma pasta tiver um diretório pai chamado PDIR, o diretório pai de PDIR será dado na coluna Pai do Diretório da linha com PDIR na \_ coluna Diretório.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>Defaultdir
</dt> <dd>

A coluna DefaultDir contém o nome do diretório (localizável)no diretório pai. Por padrão, esse é o nome dos diretórios de destino e de origem. Para especificar nomes de diretório de origem e destino diferentes, separe os nomes de destino e de origem com dois-pontos da seguinte maneira: \[ targetname \] : \[ sourcename \] .

Se o valor da coluna Pai do Diretório for nulo ou for igual à coluna Diretório, a coluna DefaultDir especificará o nome de um \_ diretório de origem raiz.

Para um diretório de origem não raiz, um ponto (.) inserido na coluna DefaultDir para o nome do diretório de origem ou o nome do diretório de destino indica que o diretório deve estar localizado em seu diretório pai sem um subdiretório.

Os nomes de diretório nessa coluna podem ser formatados como pares de nome de arquivo curtos de nome de arquivo \| longo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Cada registro na tabela representa um diretório nas imagens de origem e de destino. A tabela Diretório deve especificar um único diretório raiz com um valor de coluna Directory igual à [**propriedade TARGETDIR.**](targetdir.md)

Para uma [instalação administrativa,](administrative-installation.md)instale a imagem administrativa no diretório raiz chamado TARGETDIR e use os nomes de diretório de origem para resolver os diretórios de destino.

Observe que o instalador define várias propriedades padrão [para](properties.md) caminhos de pasta do sistema. Consulte a [Referência de](property-reference.md) Propriedade para ver uma lista das propriedades definidas como pastas do sistema.

A resolução de diretório é executada [durante a ação CostFinalize](costfinalize-action.md) e é feita da seguinte forma:

### <a name="root-destination-directory"></a>Diretório de destino raiz

Pode haver apenas um único diretório de destino raiz. Para especificar o diretório de destino raiz, depure a coluna Diretório como a [**propriedade TARGETDIR**](targetdir.md) e a coluna DefaultDir para a [**propriedade SourceDir.**](sourcedir.md) Se a **propriedade TARGETDIR** for definida, o diretório de destino será resolvido para o valor da propriedade. Se a **propriedade TARGETDIR** for indefinida, a propriedade [**ROOTDRIVE**](rootdrive.md) será usada para resolver o caminho.

### <a name="root-source-directory"></a>Diretório de origem raiz

O valor da coluna DefaultDir para a entrada do diretório raiz deve ser definido como a [**propriedade SourceDir.**](sourcedir.md)

### <a name="non-root-destination-directories"></a>Diretórios de destino não raiz

O valor de Diretório para um diretório não raiz também é interpretado como o nome de uma propriedade que define o local do destino. Se a propriedade for definida, o diretório de destino será resolvido para o valor da propriedade. Se a propriedade não estiver definida, o diretório de destino será resolvido para um subdiretório abaixo do diretório de destino resolvido para a entrada \_ Pai do Diretório. O valor DefaultDir define o nome do subdiretório.

### <a name="non-root-source-directories"></a>Diretórios de origem não raiz

O diretório de origem para um diretório não raiz é resolvido para um subdiretório do diretório de origem resolvido para a entrada \_ Pai do Diretório. Novamente, o valor DefaultDir define o nome do subdiretório.

### <a name="short-or-long-file-names"></a>Nomes de arquivo curtos ou longos

Ao resolver diretórios de destino, os nomes de arquivo curtos especificados na coluna DefaultDir serão usados se a propriedade [**SHORTFILENAMES**](shortfilenames.md) estiver definida ou se o volume no qual o diretório está localizado não dá suporte a nomes de arquivo longos. Caso contrário, o nome de arquivo longo será usado.

Observe que quando os diretórios são resolvidos durante a ação CostFinalize, as chaves na tabela Diretório tornam-se propriedades [definidas](properties.md) como caminhos de diretório.

[Tabela CreateFolder](createfolder-table.md)

Para criar pastas vazias durante uma instalação, consulte [CreateFolder Table](createfolder-table.md).

[Usando a tabela de diretório](using-the-directory-table.md)

Para obter mais informações sobre a tabela Directory, incluindo exemplos, [consulte Using the Directory Table](using-the-directory-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE56](ice56.md)  
[ICE57](ice57.md)  
[ICE64](ice64.md)  
[ICE88](ice88.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



