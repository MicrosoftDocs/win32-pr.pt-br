---
description: As linhas de uma caixa de listagem não são tratadas como controles individuais, mas fazem parte de uma caixa de listagem que funciona como um controle. A tabela ListBox define os valores para todas as caixas de listagem.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Tabela de ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922017"
---
# <a name="listbox-table"></a>Tabela de ListBox

As linhas de uma caixa de listagem não são tratadas como controles individuais, mas fazem parte de uma caixa de listagem que funciona como um controle. A tabela ListBox define os valores para todas as caixas de listagem.

A tabela ListBox tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | S   | N        |
| Ordem    | [Inteiro](integer.md)       | S   | N        |
| Valor    | [Binário](formatted.md)   | N   | N        |
| Texto     | [Binário](formatted.md)   | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

Uma propriedade nomeada a ser vinculada a este item. Todos os itens vinculados à mesma propriedade se tornam parte da mesma caixa de listagem.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene
</dt> <dd>

Um inteiro positivo usado para determinar a ordem dos itens que aparecem em uma única caixa de listagem. Se a caixa de listagem for definida como ordenada, todos os itens deverão ter um valor de pedido. Os inteiros não precisam ser consecutivos. Se a caixa de listagem for definida como não ordenada, essa coluna será ignorada.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

A cadeia de caracteres de valor associada a este item. A seleção da linha define a propriedade associada a esse valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

O texto localizável visível a ser atribuído ao item. Se essa entrada ou a coluna inteira estiver ausente, o texto assume como padrão a entrada correspondente no valor.

</dd> </dl>

## <a name="remarks"></a>Comentários

O conteúdo dos campos Value e Text são formatados pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado, portanto, eles podem conter qualquer expressão que a função **MsiFormatRecord** possa interpretar. A formatação ocorre somente quando o controle é criado e não é atualizada se uma propriedade envolvida na expressão é modificada durante a vida útil do controle.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



