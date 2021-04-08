---
description: A tabela de diretórios especifica o layout do diretório para o produto. Cada linha da tabela indica um diretório na origem e no destino.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Tabela de diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922039"
---
# <a name="directory-table"></a>Tabela de diretórios

A tabela de diretórios especifica o layout do diretório para o produto. Cada linha da tabela indica um diretório na origem e no destino.

A tabela de diretórios tem as colunas a seguir.



| Coluna            | Tipo                         | Chave | Nullable |
|-------------------|------------------------------|-----|----------|
| Diretório         | [Identificador](identifier.md) | S   | N        |
| Pai do diretório \_ | [Identificador](identifier.md) | N   | S        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Active
</dt> <dd>

A coluna Directory contém um identificador exclusivo para um diretório ou caminho de diretório. Essa coluna pode conter o nome de uma propriedade que é definida como o caminho completo de um diretório de destino. Se essa coluna contiver uma propriedade, o diretório de destino usará o nome especificado na coluna DefaultDir e usará o diretório pai especificado na \_ coluna pai do diretório.

O diretório de origem sempre usa o nome especificado na coluna DefaultDir e usa o diretório pai especificado na \_ coluna pai do diretório.

Se a \_ coluna pai do diretório for nula ou igual ao valor da coluna diretório, a coluna diretório representará um diretório de destino raiz. Somente um diretório raiz pode ser especificado na tabela de diretórios.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Pai do diretório \_
</dt> <dd>

Esta coluna é uma referência ao diretório pai do diretório. Um registro que tem uma \_ coluna pai de diretório igual a NULL ou igual à coluna de diretório representa um diretório raiz. O caminho completo do diretório pai é resolvido por referência na \_ coluna pai do diretório é uma chave externa na coluna diretório. Por exemplo, se uma pasta tiver um diretório pai chamado PDIR, o diretório pai de PDIR será fornecido na \_ coluna pai do diretório da linha com PDIR na coluna Directory.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

A coluna DefaultDir contém o nome do diretório (localizável) no diretório pai. Por padrão, esse é o nome dos diretórios de destino e de origem. Para especificar nomes de diretórios de origem e de destino diferentes, separe os nomes de origem e de destino com dois-pontos da seguinte maneira: \[ TargetName \] : \[ SourceName \] .

Se o valor da \_ coluna pai do diretório for nulo ou for igual à coluna do diretório, a coluna DefaultDir especificará o nome de um diretório de origem raiz.

Para um diretório de origem não raiz, um ponto (.) inserido na coluna DefaultDir para o nome do diretório de origem ou o nome do diretório de destino indica que o diretório deve estar localizado em seu diretório pai sem um subdiretório.

Os nomes de diretório nesta coluna podem ser formatados como pares curtos de nome de arquivo \| .

</dd> </dl>

## <a name="remarks"></a>Comentários

Cada registro na tabela representa um diretório nas imagens de origem e de destino. A tabela de diretórios deve especificar um único diretório raiz com um valor de coluna de diretório igual à propriedade [**TARGETDIR**](targetdir.md) .

Para uma [instalação administrativa](administrative-installation.md), instale a imagem administrativa no diretório raiz chamado TARGETDIR e use os nomes de diretório de origem para resolver os diretórios de destino.

Observação o instalador define um número de [Propriedades](properties.md) padrão para caminhos de pasta do sistema. Consulte a [referência de propriedade](property-reference.md) para obter uma lista das propriedades definidas como pastas do sistema.

A resolução de diretório é executada durante a [ação CostFinalize](costfinalize-action.md) e é feita da seguinte maneira:

### <a name="root-destination-directory"></a>Diretório de destino raiz

Pode haver apenas um único diretório de destino raiz. Para especificar o diretório de destino raiz, defina a coluna Directory como a propriedade [**TARGETDIR**](targetdir.md) e a coluna DefaultDir como a propriedade [**SourceDir**](sourcedir.md) . Se a propriedade **TARGETDIR** for definida, o diretório de destino será resolvido para o valor da propriedade. Se a propriedade **TARGETDIR** for indefinida, a propriedade [**ROOTDRIVE**](rootdrive.md) será usada para resolver o caminho.

### <a name="root-source-directory"></a>Diretório de origem raiz

O valor da coluna DefaultDir para a entrada do diretório raiz deve ser definido como a propriedade [**SourceDir**](sourcedir.md) .

### <a name="non-root-destination-directories"></a>Diretórios de destino não raiz

O valor do diretório para um diretório não raiz também é interpretado como o nome de uma propriedade que define o local do destino. Se a propriedade for definida, o diretório de destino será resolvido para o valor da propriedade. Se a propriedade não for definida, o diretório de destino será resolvido para um subdiretório abaixo do diretório de destino resolvido para a \_ entrada pai do diretório. O valor DefaultDir define o nome do subdiretório.

### <a name="non-root-source-directories"></a>Diretórios de origem não raiz

O diretório de origem para um diretório não raiz é resolvido para um subdiretório do diretório de origem resolvido para a \_ entrada pai do diretório. Novamente, o valor DefaultDir define o nome do subdiretório.

### <a name="short-or-long-file-names"></a>Nomes de arquivo curtos ou longos

Ao resolver os diretórios de destino, os nomes de arquivo curtos especificados na coluna DefaultDir são usados se a propriedade [**SHORTFILENAMES**](shortfilenames.md) é definida ou o volume no qual o diretório está localizado não dá suporte a nomes de arquivo longos. Caso contrário, o nome de arquivo longo será usado.

Observe que, quando os diretórios são resolvidos durante a ação CostFinalize, as chaves na tabela de diretórios tornam-se [Propriedades](properties.md) definidas como caminhos de diretório.

[Tabela CreateFolder](createfolder-table.md)

Para criar pastas vazias durante uma instalação, consulte a [tabela CreateFolder](createfolder-table.md).

[Usando a tabela de diretórios](using-the-directory-table.md)

Para obter mais informações sobre a tabela de diretórios, incluindo exemplos, consulte [usando a tabela de diretórios](using-the-directory-table.md).

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

 

 



