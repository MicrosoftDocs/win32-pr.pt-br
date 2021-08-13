---
description: A tabela ModuleSubstitution especifica os campos configuráveis de um banco de dados de módulo e fornece um modelo para a configuração de cada campo.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Tabela ModuleSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66fbbb0898a254b181d02eca78f33709f8c0e037de140a37893ea3887af6390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628578"
---
# <a name="modulesubstitution-table"></a>Tabela ModuleSubstitution

A tabela ModuleSubstitution especifica os campos configuráveis de um banco de dados de módulo e fornece um modelo para a configuração de cada campo. O usuário ou a ferramenta de mesclagem pode consultar essa tabela para determinar quais operações de configuração serão realizadas. Essa tabela não é mesclada no banco de dados de destino.

As tabelas a seguir não podem conter campos configuráveis e não devem ser listadas nesta tabela:

Tabela ModuleSubstitution

[Tabela ModuleConfiguration](moduleconfiguration-table.md)

[Tabela ModuleExclusion](moduleexclusion-table.md)

[Tabela ModuleSignature](modulesignature-table.md)

A tabela ModuleSubstitution tem as seguintes colunas.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Tabela  | [Identificador](identifier.md) | Y   | N        |
| Linha    | [Text](text.md)             | Y   | N        |
| Coluna | [Identificador](identifier.md) | Y   | N        |
| Valor  | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Essa coluna especifica o nome da tabela que está sendo modificada no banco de dados do módulo.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Linha
</dt> <dd>

Esse campo especifica as chaves primárias da linha de destino na tabela chamada na coluna Tabela. Várias chaves primárias são separadas por ponto e vírgula. As linhas de destino são selecionadas para modificação antes que todas as alterações sejam feitas na tabela de destino. Se um registro na tabela ModuleSubstitution mudar o campo de chave primária de uma linha de destino, outros registros na tabela ModuleSubstitution serão aplicados com base nos dados originais da chave primária, não no resultado de substituições de chave primária. A ordem de substituição de linha é indefinida.

Os valores nesta coluna estão sempre no [formato especial do CMSM](cmsm-special-format.md). Um ponto e vírgula literal (';') ou sinal de igual ('=') pode ser adicionado prefixando o caractere com uma faixa invertida. '\\'. Um valor nulo para uma chave é significado por um nulo, um ponto e vírgula à esquerda, dois ponto e vírgula consecutivos ou um ponto e vírgula à direita, dependendo se o valor nulo é um valor exclusivo, primeiro, intermediário ou final da coluna de chave.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Coluna
</dt> <dd>

Esse campo especifica a coluna de destino na linha nomeada na coluna Linha. Se várias linhas na tabela ModuleSubstitution alterarem colunas diferentes da mesma linha de destino, todas as substituições de coluna serão executadas antes que a linha modificada seja inserida no banco de dados. A ordem de substituição de coluna é indefinida.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Essa coluna contém uma cadeia de caracteres que fornece um modelo de formatação para os dados que estão sendo substituídos no campo de destino especificado por Tabela, Linha e Coluna. Quando uma cadeia de caracteres de substituição do formato =ItemA é encontrada, a cadeia de caracteres, incluindo os caracteres de colchete, é substituída pelo valor do \[ \] "ItemA" configurável. O item configurável "ItemA" é especificado na coluna Nome da tabela [ModuleConfiguration](moduleconfiguration-table.md) e seu valor é fornecido pela ferramenta de mesclagem. Se a ferramenta de mesclagem recusar a fornecer um valor para qualquer item em uma cadeia de caracteres de substituição, o valor padrão especificado na coluna DefaultValue da Tabela ModuleConfiguration será substituído. Se uma cadeia de caracteres referenciar um item que não está na tabela ModuleConfiguration, a mesclagem falhará.

-   Esta coluna usa [o formato especial do CMSM](cmsm-special-format.md). Um ponto e vírgula literal (';') ou um sinal de igual ('=') pode ser adicionado à tabela prefixando o caractere com uma faixa invertida. '\\'.
-   O campo Valor pode conter várias cadeias de caracteres de substituição. Por exemplo, a configuração dos itens "Food1" e "Food2" na cadeia de caracteres: " =Food1 é boa, mas =Food2 é melhor porque =Food2 é mais \[ \] \[ \] \[ \] descarado".
-   As cadeias de caracteres de substituição não devem ser aninhadas. O modelo " \[ =AB \[ =CDE \] \] " é inválido.
-   Se o campo Valor for avaliada como nula e o campo de destino não for anulado, a mesclagem falhará e um objeto de erro do tipo msmErrorBadNullSubstitution será criado e adicionado à lista de erros. Para obter detalhes, consulte os tipos de erro descritos em [**get \_ Type Function**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).
-   Se o campo Valor for avaliada como o GUID nulo: , o GUID nulo será substituído pelo nome do recurso antes que a linha seja {00000000-0000-0000-0000-000000000000} mesclada no módulo. Para obter detalhes, consulte [Referenciando recursos em módulos de mesclagem](referencing-features-in-merge-modules.md).
-   O modelo no campo Valor é avaliado antes de ser inserido no campo de destino. A substituição em uma linha é feita antes de substituir os recursos.
-   Se a coluna Valor for avaliada como uma cadeia de caracteres de apenas caracteres inteiros (com um + ou -opcional), a cadeia de caracteres será convertida em um inteiro antes de ser substituída em um campo de destino do Tipo de Formato [Inteiro](integer-format-types.md). Se o modelo for avaliada como uma cadeia de caracteres que não consiste apenas em caracteres inteiros (e um + ou -opcional), o resultado não poderá ser substituído em um campo de destino inteiro. Tentar inserir um não inteiro em um campo inteiro faz com que a mesclagem falhe e adiciona um objeto de erro msmErrorBadSubstitutionType à lista de erros.
-   Se [a](text-format-types.md)coluna de destino especificada nos campos Tabela e Coluna for um Tipo de Formato de Texto e a avaliação do campo Valor resulta em um Tipo de Formato Inteiro [,](integer-format-types.md)uma representação decimal do número será inserida no campo de texto de destino.
-   Se o campo [](integer-format-types.md)de destino for um Tipo de Formato inteiro e o campo Valor consistir em uma lista não delimitada de itens no formato  [Bitfield](bitfield-format-types.md), o valor no campo de destino será combinado usando o operador **AND** bit a bit com o inverso do OR bit a bit de todos os valores de máscara dos itens e, em seguida, combinado usando o operador **OR** bit a bit com cada um dos itens inteiros ou bitfield quando mascarados por seus valores de máscara correspondentes. Essencialmente, isso define explicitamente os bits das propriedades para os valores fornecidos, mas deixa todos os outros bits na célula sozinhos.
-   Se o campo Valor [](key-format-types.md)for avaliada como um Tipo de Formato de Chave e for uma chave em uma tabela que usa várias chaves primárias, o nome do item poderá ser seguido por um ponto e vírgula e um valor inteiro que indica o índice baseado em 1 no conjunto de valores que juntos fazem uma chave primária. Se nenhum inteiro for especificado, o valor 1 será usado. Por exemplo, a [tabela Controle tem](control-table.md) duas colunas de chave primária, Diálogo e \_ Controle. O valor de um item "Item1" que é uma chave na tabela Control será do formato "DialogName; ControlName", em que DialogName é o valor na tabela Dialog \_ e ControlName é o valor na coluna Controle. Para substituir apenas ControlName, a cadeia de caracteres \[ de substituição =Item1;2 \] deve ser usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

A tabela ModuleSubstition é usada por [Módulos de Mesclagem Configuráveis.](configurable-merge-modules.md) Mergemod.dll versão 2.0 ou posterior é necessária para criar um módulo de mesclagem configurável.

Para garantir a compatibilidade com versões do Mergemod.dll anteriores à versão 2.0, as tabelas [ModuleConfiguration](moduleconfiguration-table.md) e ModuleSubstitution devem ser incluídas na tabela [ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.

 

 
