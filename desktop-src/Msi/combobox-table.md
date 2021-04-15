---
description: As linhas de uma caixa de combinação não são tratadas como controles individuais; Eles fazem parte de uma única caixa de combinação que funciona como um controle. Esta tabela lista os valores para cada caixa de combinação.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Tabela ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747347"
---
# <a name="combobox-table"></a>Tabela ComboBox

As linhas de uma caixa de combinação não são tratadas como controles individuais; Eles fazem parte de uma única caixa de combinação que funciona como um controle. Esta tabela lista os valores para cada caixa de combinação.

A tabela ComboBox tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | S   | N        |
| Ordem    | [Inteiro](integer.md)       | S   | N        |
| Valor    | [Binário](formatted.md)   | N   | N        |
| Texto     | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

Uma propriedade nomeada a ser vinculada a este item. Todos os itens vinculados à mesma propriedade se tornam parte da mesma caixa de combinação.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene
</dt> <dd>

Um inteiro positivo usado para determinar a ordem dos itens que aparecem em uma única lista de caixas de combinação. Os inteiros não precisam ser consecutivos. Se uma caixa de combinação for definida como ordenada, todos os itens deverão ter um valor de pedido. Se a caixa de combinação for definida como não ordenada, essa coluna será ignorada.

Somente números positivos.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

A cadeia de caracteres de valor associada a este item. A seleção dessa linha da caixa de combinação define a propriedade associada (especificada na propriedade) para esse valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

O texto que está visível e localizável a ser atribuído ao item. Se essa entrada ou a coluna inteira estiver ausente, o texto padrão será a entrada em valor.

</dd> </dl>

## <a name="remarks"></a>Comentários

O conteúdo dos campos Value e Text são formatados pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado, portanto, eles podem conter qualquer expressão que a função **MsiFormatRecord** possa interpretar. A formatação ocorre somente quando o controle é criado e não é atualizado se uma propriedade envolvida na expressão é modificada durante a vida útil do controle.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



