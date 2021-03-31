---
description: A tabela ModuleSubstitution especifica os campos configuráveis de um banco de dados de módulo e fornece um modelo para a configuração de cada campo.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Tabela ModuleSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e27789f723af87e228bada91b79a16d7dc4d2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172025"
---
# <a name="modulesubstitution-table"></a>Tabela ModuleSubstitution

A tabela ModuleSubstitution especifica os campos configuráveis de um banco de dados de módulo e fornece um modelo para a configuração de cada campo. A ferramenta de usuário ou de mesclagem pode consultar essa tabela para determinar quais operações de configuração devem ocorrer. Esta tabela não é mesclada no banco de dados de destino.

As tabelas a seguir não podem conter campos configuráveis e não devem estar listadas nesta tabela:

Tabela ModuleSubstitution

[Tabela ModuleConfiguration](moduleconfiguration-table.md)

[Tabela ModuleExclusion](moduleexclusion-table.md)

[Tabela ModuleSignature](modulesignature-table.md)

A tabela ModuleSubstitution tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Tabela  | [Identificador](identifier.md) | S   | N        |
| Linha    | [Text](text.md)             | S   | N        |
| Coluna | [Identificador](identifier.md) | S   | N        |
| Valor  | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Esta coluna especifica o nome da tabela que está sendo modificada no banco de dados do módulo.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila
</dt> <dd>

Este campo especifica as chaves primárias da linha de destino na tabela denominada na coluna tabela. Várias chaves primárias são separadas por ponto e vírgula. Linhas de destino são selecionadas para modificação antes que qualquer alteração seja feita na tabela de destino. Se um registro na tabela ModuleSubstitution alterar o campo de chave primária de uma linha de destino, outros registros na tabela ModuleSubstitution serão aplicados com base nos dados da chave primária original, não no resultado de substituições de chave primária. A ordem de substituição de linha é indefinida.

Os valores nesta coluna estão sempre no [formato especial CMSM](cmsm-special-format.md). Um ponto-e-vírgula literal ('; ') ou sinal de igual (' = ') pode ser adicionado por meio da prefixação do caractere com uma barra invertida. '\\'. Um valor nulo para uma chave é representado por um caractere nulo, um ponto-e-vírgula à esquerda, dois pontos-e-vírgulas consecutivos ou um ponto e vírgula à direita, dependendo se o valor nulo é um valor de coluna de chave único, primeiro, médio ou final.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Pilha
</dt> <dd>

Este campo especifica a coluna de destino na linha denominada na coluna linha. Se várias linhas na tabela ModuleSubstitution alterarem colunas diferentes da mesma linha de destino, todas as substituições de coluna serão executadas antes que a linha modificada seja inserida no banco de dados. A ordem de substituição de coluna é indefinida.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Esta coluna contém uma cadeia de caracteres que fornece um modelo de formatação para os dados que estão sendo substituídos no campo de destino especificado por tabela, linha e coluna. Quando uma cadeia de caracteres de substituição do formulário \[ = Itema \] for encontrada, a cadeia de caracteres, incluindo os caracteres de colchete, será substituída pelo valor para o "Itema" configurável. O item configurável "Itema" é especificado na coluna Name da [Tabela ModuleConfiguration](moduleconfiguration-table.md) e seu valor é fornecido pela ferramenta de mesclagem. Se a ferramenta de mesclagem declinar para fornecer um valor para qualquer item em uma cadeia de caracteres de substituição, o valor padrão especificado na coluna DefaultValue da Tabela ModuleConfiguration será substituído. Se uma cadeia de caracteres fizer referência a um item que não está na Tabela ModuleConfiguration, a mesclagem falhará.

-   Essa coluna usa o [formato especial CMSM](cmsm-special-format.md). Um ponto-e-vírgula literal ('; ') ou sinal de igual (' = ') pode ser adicionado à tabela por meio da prefixação do caractere com uma barra invertida. '\\'.
-   O campo valor pode conter várias cadeias de caracteres de substituição. Por exemplo, a configuração dos itens "Food1" e "Food2" na cadeia de caracteres: " \[ = Food1 \] é boa, mas \[ = Food2 \] é melhor porque \[ = Food2 \] é mais nutritious".
-   As cadeias de caracteres de substituição não devem ser aninhadas. O modelo " \[ = AB \[ = CDE \] \] " é inválido.
-   Se o campo valor for avaliado como nulo e o campo de destino não for anulável, a mesclagem falhará e um objeto de erro do tipo msmErrorBadNullSubstitution será criado e adicionado à lista de erros. Para obter detalhes, consulte os tipos de erro descritos na [**\_ função obter tipo**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).
-   Se o campo de valor for avaliado como o GUID NULL: {00000000-0000-0000-0000-000000000000} , o GUID NULL será substituído pelo nome do recurso antes que a linha seja mesclada no módulo. Para obter detalhes, consulte [Referenciando recursos em módulos de mesclagem](referencing-features-in-merge-modules.md).
-   O modelo no campo valor é avaliado antes de ser inserido no campo de destino. A substituição em uma linha é feita antes da substituição de qualquer recurso.
-   Se a coluna de valor for avaliada como uma cadeia de caracteres de somente números inteiros (com um opcional + ou-), a cadeia de caracteres será convertida em um inteiro antes de ser substituída em um campo de destino do [tipo de formato inteiro](integer-format-types.md). Se o modelo for avaliado como uma cadeia de caracteres que não consiste apenas em caracteres inteiros (e um opcional + ou-), o resultado não poderá ser substituído em um campo de destino de inteiro. A tentativa de inserir um não inteiro em um campo inteiro faz com que a mesclagem falhe e adicione um objeto de erro msmErrorBadSubstitutionType à lista de erros.
-   Se a coluna de destino especificada nos campos de tabela e coluna for um [tipo de formato de texto](text-format-types.md), e a avaliação do campo valor resultar em um tipo de [formato inteiro](integer-format-types.md), uma representação decimal do número será inserida no campo de texto de destino.
-   Se o campo de destino for [um tipo de formato inteiro](integer-format-types.md), e o campo de valor consiste em uma lista não delimitada de itens no [formato](bitfield-format-types.md)de campo de bits, o valor no campo de destino é combinado usando o operador **and** bit a bit com o inverso de or de-bit **ou** de todos os valores de máscara dos itens e, em seguida, combinado usando **o operador OR** de inteiros com cada um dos itens de inteiro ou de campo de ocultação quando Essencialmente, isso define explicitamente os bits das propriedades para os valores fornecidos, mas deixa todos os outros bits somente na célula.
-   Se o campo valor for avaliado como um [tipo de formato de chave](key-format-types.md)e for uma chave em uma tabela que usa várias chaves primárias, o nome do item poderá ser seguido por um ponto e vírgula e um valor inteiro que indica o índice de base 1 no conjunto de valores que juntos fazem uma chave primária. Se nenhum inteiro for especificado, o valor 1 será usado. Por exemplo, a [tabela de controle](control-table.md) tem duas colunas de chave primária, caixa \_ de diálogo e controle. O valor de um item "Item1" que é uma chave para a tabela de controle estará no formato "Dialogname; ControlName ", em que Dialogname é o valor na tabela de diálogo \_ e ControlName é o valor na coluna Control. Para substituir apenas ControlName, a cadeia de caracteres de substituição \[ = Item1; 2 \] deve ser usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

A tabela ModuleSubstition é usada por [módulos de mesclagem configuráveis](configurable-merge-modules.md). Mergemod.dll versão 2,0 ou posterior é necessária para criar um módulo de mesclagem configurável.

Para garantir a compatibilidade com versões do Mergemod.dll anteriores à versão 2,0, a [Tabela ModuleConfiguration](moduleconfiguration-table.md) e as tabelas ModuleSubstitution devem ser incluídas na [tabela ModuleIgnoreTable](moduleignoretable-table.md) de cada módulo.

 

 
