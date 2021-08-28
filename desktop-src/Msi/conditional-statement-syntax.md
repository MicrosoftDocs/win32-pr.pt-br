---
description: Esta seção descreve a sintaxe de instruções condicionais usadas pela função MsiEvaluateCondition e as tabelas de sequência de ação. Para obter mais informações, consulte exemplos de sintaxe de instrução condicional.
ms.assetid: 6f1657f9-063b-4d57-ad76-95e3dbe25786
title: Sintaxe de instrução condicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131cf9513d4bf19bb84c5777d1fed1411a682ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886439"
---
# <a name="conditional-statement-syntax"></a>Sintaxe de instrução condicional

Esta seção descreve a sintaxe de instruções condicionais usadas pela função [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) e as [tabelas de sequência](using-a-sequence-table.md)de ação. Para obter mais informações, consulte [exemplos de sintaxe de instrução condicional](examples-of-conditional-statement-syntax.md).

## <a name="summary-of-conditional-statement-syntax"></a>Resumo da sintaxe da instrução condicional

Essa tabela e a lista a seguir resumem a sintaxe a ser usada em expressões condicionais.



| Item                | Syntax                                                                                                          |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
| value               | \|inteiro literal de símbolo \|                                                                                    |
| operador de comparação | < \| > \| <= \| >= \| = \| <>                                                                 |
| Termo                | valor \| do valor Comparison-operador value \| (expressão)\|                                                    |
| Fator booliano      | termo \| **não** termo                                                                                            |
| Termo booliano        | \|Booliano booleano-fator **e** termo                                                                   |
| expressão          | Valor booliano do termo booliano \| **ou** expressão                                                                  |
| símbolo              | Propriedade \| % Environment-variável \| $Component-Action \| ? estado do componente \| &recurso-ação \| ! recurso-estado |



 

-   Os valores e nomes de símbolos diferenciam maiúsculas de minúsculas.
-   Os nomes de variáveis de ambiente não diferenciam maiúsculas de minúsculas.
-   O texto literal deve ser colocado entre aspas ("text").
    > [!Note]  
    > O texto literal contendo aspas não pode ser usado em instruções condicionais porque não há caractere de escape para aspas dentro do texto literal. Para fazer uma comparação com o texto literal contendo aspas, o texto literal deve ser colocado em uma propriedade. Por exemplo, para verificar se a propriedade SERVERname não contém aspas, defina uma propriedade chamada QUOTes na tabela de [Propriedades](property-table.md) com um valor de "e altere a condição para não servername><aspas.

     

-   Valores de propriedade inexistentes são tratados como cadeias de caracteres vazias.
-   Não há suporte para valores numéricos de ponto flutuante.
-   os operadores e a precedência são os mesmos das linguagens básica e SQL.
-   Não há suporte para operadores aritméticos.
-   Os parênteses podem ser usados para substituir a precedência do operador.
-   Os operadores não diferenciam maiúsculas de minúsculas.
-   Para comparações de cadeia de caracteres, um til "~" prefixado para o operador executa uma comparação que não diferencia maiúsculas de minúsculas.
-   A comparação de um inteiro com uma cadeia de caracteres ou um valor de propriedade que não pode ser convertido em um inteiro é sempre **msiEvaluateConditionFalse**, exceto pelo operador de comparação "<>", que retorna **msiEvaluateConditionTrue**.

## <a name="access-prefixes"></a>Prefixos de acesso

A tabela a seguir mostra os prefixos a serem usados para acessar várias informações do sistema e do instalador para uso em expressões condicionais.



| Tipo de símbolo          | Prefixo | Valor                                                     |
|----------------------|--------|-----------------------------------------------------------|
| Propriedade do instalador   | (nenhum) | Valor da tabela de propriedade ([Propriedade](property-table.md)). |
| Variável de ambiente | %      | Valor da variável de ambiente.                            |
| Chave de tabela de componentes  | $      | Estado de ação do componente.                            |
| Chave de tabela de componentes  | ?      | Estado de instalação do componente.                         |
| Chave da tabela de recursos    | &      | Estado de ação do recurso.                              |
| Chave da tabela de recursos    | !      | Estado instalado do recurso.                           |



 

## <a name="logical-operators"></a>Operadores lógicos

A tabela a seguir mostra os operadores lógicos em expressões condicionais, em ordem de precedência de alto para baixo.



| Operador | Significado                                                 |
|----------|---------------------------------------------------------|
| Not      | Operador unário de prefixo; inverte o estado do termo a seguir. |
| E      | TRUE se ambos os termos forem verdadeiros.                            |
| Ou       | TRUE se um ou ambos os termos forem verdadeiros.                  |
| Xor      | TRUE se nenhum dos dois termos for verdadeiro.             |
| Eqv      | TRUE se ambos os termos forem verdadeiros ou ambos os termos forem falsos.    |
| IMP      | TRUE se o termo esquerdo for FALSE ou o termo direito for TRUE.       |



 

## <a name="comparative-operators"></a>Operadores comparativaes

A tabela a seguir mostra os operadores de comparação usados em expressões condicionais. Esses operadores de comparação só podem ocorrer entre dois valores.



| Operador | Significado                                                     |
|----------|-------------------------------------------------------------|
| =        | VERDADEIRO se o valor esquerdo for igual ao valor correto.                 |
| <> | VERDADEIRO se o valor esquerdo não for igual ao valor correto.             |
| >     | VERDADEIRO se o valor esquerdo for maior que o valor correto.             |
| >=    | VERDADEIRO se o valor esquerdo for maior ou igual ao valor correto. |
| <     | TRUE se o valor Left for menor que o valor Right.                |
| <=    | VERDADEIRO se o valor esquerdo for menor ou igual ao valor correto.    |



 

## <a name="substring-operators"></a>Operadores de subcadeia de caracteres

A tabela a seguir mostra os operadores de subcadeia de caracteres usados em expressões condicionais. Operadores de subcadeia de caracteres podem ocorrer entre dois valores de cadeia de caracteres.



| Operador | Significado                                           |
|----------|---------------------------------------------------|
| >< | TRUE se a cadeia de caracteres esquerda contiver a cadeia de caracteres correta.    |
| << | TRUE se a cadeia de caracteres esquerda começar com a cadeia de caracteres correta. |
| >> | TRUE se a cadeia de caracteres esquerda terminar com a cadeia de caracteres correta.   |



 

## <a name="bitwise-numeric-operators"></a>Operadores numéricos bits

A tabela a seguir mostra os operadores numéricos de bits em expressões condicionais. Esses operadores podem ocorrer entre dois valores inteiros.



| Operador | Significado                                                                      |
|----------|------------------------------------------------------------------------------|
| >< | AND bit e, TRUE se os inteiros esquerdo e direito tiverem quaisquer bits em comum.    |
| << | True se os 16 bits altos do inteiro esquerdo forem iguais ao inteiro correto. |
| >> | True se os 16 bits baixos do inteiro esquerdo forem iguais ao inteiro correto.  |



 

## <a name="feature-and-component-state-values"></a>Valores de estado de componente e recurso

A tabela a seguir mostra onde é válido usar os símbolos de operador de componente e recurso.



| Estado do operador &lt;&gt; | Onde essa sintaxe é válida                                                                                                                                         |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ação de $component      | Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) . |
| Recurso de &-ação        | Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) . |
| ! recurso-estado         | Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) . |
| ? Estado do componente       | Na tabela [condição](condition-table.md) , e nas tabelas de [sequência](using-a-sequence-table.md) , após a ação [CostFinalize](costfinalize-action.md) . |



 

A tabela a seguir mostra os valores de estado do componente e do recurso usados em expressões condicionais. Esses Estados não são definidos até que [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) seja chamado, seja diretamente ou pela ação [CostFinalize](costfinalize-action.md) .



| Estado                    | Valor | Significado                                                         |
|--------------------------|-------|-----------------------------------------------------------------|
| INSTALLstate \_ desconhecido    | -1    | Nenhuma ação a ser executada no recurso ou componente.              |
| INSTALLstate \_ anunciado | 1     | Recurso anunciado. Esse estado não está disponível para os componentes do. |
| INSTALLstate \_ ausente     | 2     | O recurso ou componente não está presente.                            |
| INSTALAR \_ local      | 3     | Recurso ou componente no computador local.                     |
| origem de INSTALLstate \_     | 4     | Execução de recurso ou componente da origem.                       |



 

Por exemplo, a expressão condicional "&MyFeature = 3" será avaliada como true somente se MyFeature estiver mudando de seu estado atual para o estado de ser instalado no computador local, INSTALLstate \_ local.

Observe que você não deve depender da condição $Component 1 = 3 para verificar se o Component1 está instalado localmente no computador. Isso poderá falhar se o Component1 for instalado por mais de um produto. Depois que o Component1 tiver sido instalado localmente pelo Product1, o instalador avaliará a condição $Component 1 = 3 como false durante a instalação do Product2. Isso ocorre porque o instalador determina a versão do componente usando o caminho de chave do componente e marca o componente para instalação se sua versão for maior ou igual ao componente instalado.

Observe que o instalador não fará comparações diretas do tipo de dados [version](version.md) em instruções condicionais. Por exemplo, você não pode usar operadores comparativa para comparar versões como "1,10" e "1, 10" em uma instrução condicional. Em vez disso, use um método válido para pesquisar uma versão, como descrito em [pesquisando aplicativos existentes, arquivos, entradas de registro ou .ini entradas de arquivo](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)e, em seguida, defina uma propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md)
</dt> </dl>

 

 



