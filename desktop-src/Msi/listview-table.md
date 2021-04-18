---
description: As linhas de ListView não são tratadas como controles individuais, mas fazem parte de um ListView que funciona como um controle. A tabela ListView define os valores para todos os ListViews.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tabela ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770192"
---
# <a name="listview-table"></a>Tabela ListView

As linhas de ListView não são tratadas como controles individuais, mas fazem parte de um ListView que funciona como um controle. A tabela ListView define os valores para todos os ListViews.

A tabela ListView tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | S   | N        |
| Ordem    | [Inteiro](integer.md)       | S   | N        |
| Valor    | [Binário](formatted.md)   | N   | N        |
| Texto     | [Binário](formatted.md)   | N   | S        |
| Binário\_ | [Identificador](identifier.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

Uma propriedade nomeada a ser vinculada a este item. Todos os itens vinculados à mesma propriedade se tornam parte do mesmo ListView.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene
</dt> <dd>

Um inteiro positivo usado para determinar a ordem dos itens que aparecem em uma única lista de ListView. Os inteiros não precisam ser consecutivos. Se um ListView for definido como ordenado, todos os itens deverão ter um valor de ordenação. Se ListView for definido como não ordenado, essa coluna será ignorada.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

A cadeia de caracteres de valor associada a este item. A seleção da linha define a propriedade associada a esse valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

O texto que está visível e localizável a ser atribuído ao item. Se essa entrada ou a coluna inteira estiver ausente, o texto usa como padrão a entrada correspondente no valor.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binário\_
</dt> <dd>

Os dados da imagem para o ícone. Esta é uma chave estrangeira para a [tabela binária](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

O conteúdo dos campos Value e Text são formatados pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado, portanto, eles podem conter qualquer expressão que a função MsiFormatRecord possa interpretar. A formatação ocorre somente quando o controle é criado e não é atualizada se uma propriedade envolvida na expressão é modificada durante a vida útil do controle.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



