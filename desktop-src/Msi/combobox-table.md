---
description: As linhas de uma caixa de combinação não são tratadas como controles individuais; eles fazem parte de uma única caixa de combinação que funciona como um controle. Esta tabela lista os valores de cada caixa de combinação.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Tabela ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea20677ab6ede02f76a1061d5f715eb0b8d6d87a1744d1eb89b7e0918a018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380291"
---
# <a name="combobox-table"></a>Tabela ComboBox

As linhas de uma caixa de combinação não são tratadas como controles individuais; eles fazem parte de uma única caixa de combinação que funciona como um controle. Esta tabela lista os valores de cada caixa de combinação.

A tabela ComboBox tem as seguintes colunas.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | Y   | N        |
| Ordem    | [Inteiro](integer.md)       | Y   | N        |
| Valor    | [Formatado](formatted.md)   | N   | N        |
| Texto     | [Text](text.md)             | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

Uma propriedade nomeada a ser vinculada a este item. Todos os itens vinculados à mesma propriedade tornam-se parte da mesma caixa de combinação.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordem
</dt> <dd>

Um inteiro positivo usado para determinar a ordenação dos itens que aparecem em uma única lista de caixas de combinação. Os inteiros não devem ser consecutivos. Se uma caixa de combinação for definida como ordenada, todos os itens deverão ter um valor Order. Se a caixa de combinação for definida como nãoordenada, essa coluna será ignorada.

Somente números positivos.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

A cadeia de caracteres de valor associada a este item. Selecionar essa linha da caixa de combinação define a propriedade associada (especificada em Propriedade) para esse valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

O texto visível e localizável a ser atribuído ao item. Se essa entrada ou a coluna inteira estiver ausente, o texto assume como padrão a entrada em Valor.

</dd> </dl>

## <a name="remarks"></a>Comentários

O conteúdo dos campos Valor e Texto é formatado pela [**função MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado, portanto, eles podem conter qualquer expressão que a **função MsiFormatRecord** possa interpretar. A formatação ocorre somente quando o controle é criado e não é atualizado se uma propriedade envolvida na expressão é modificada durante a vida útil do controle.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



