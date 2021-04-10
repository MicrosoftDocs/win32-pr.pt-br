---
description: Os botões de opção não são tratados como controles individuais, mas fazem parte de um grupo de botões de opção que funciona como um controle de botão de seleção. A tabela RadioButton lista os botões para todos os grupos.
ms.assetid: 7f8f278a-a737-4116-9938-2850dbb611fa
title: Tabela de botões de opção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097f8fbe3081c865e3668631ed0fa9d43a4488cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169390"
---
# <a name="radiobutton-table"></a>Tabela de botões de opção

Os botões de opção não são tratados como controles individuais, mas fazem parte de um grupo de botões de opção que funciona como um [controle](radiobuttongroup-control.md)de botão de seleção. A tabela RadioButton lista os botões para todos os grupos.

A tabela RadioButton tem as colunas a seguir.



| Coluna   | Tipo                         | Chave | Nullable |
|----------|------------------------------|-----|----------|
| Propriedade | [Identificador](identifier.md) | S   | N        |
| Ordem    | [Inteiro](integer.md)       | S   | N        |
| Valor    | [Binário](formatted.md)   | N   | N        |
| X        | [Inteiro](integer.md)       | N   | N        |
| S        | [Inteiro](integer.md)       | N   | N        |
| Largura    | [Inteiro](integer.md)       | N   | N        |
| Altura   | [Inteiro](integer.md)       | N   | N        |
| Texto     | [Binário](formatted.md)   | N   | S        |
| Ajuda     | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

Uma propriedade nomeada a ser vinculada a este botão de opção. Todos os botões vinculados à mesma propriedade se tornam parte do mesmo grupo.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene
</dt> <dd>

Um inteiro positivo usado para determinar a ordem dos itens em uma lista. Os inteiros não precisam ser consecutivos.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

A cadeia de caracteres de valor associada a este botão. Selecionar o botão define a propriedade associada para esse valor.

</dd> <dt>

<span id="X"></span><span id="x"></span>W.x.y.
</dt> <dd>

A coordenada horizontal dentro do grupo do canto superior esquerdo do retângulo delimitador do botão de opção. Este deve ser um número não negativo.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Iar
</dt> <dd>

A coordenada vertical dentro do grupo do canto superior esquerdo do retângulo delimitador do botão de opção. Este deve ser um número não negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largura
</dt> <dd>

A largura do botão. Este deve ser um número não negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Tamanho
</dt> <dd>

A altura do botão. Este deve ser um número não negativo.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

O título localizável visível a ser atribuído ao botão de opção. Se o texto for muito longo para caber no controle, ele será truncado. Se o botão exibir um ícone ou um bitmap, essa coluna conterá o nome da imagem, que é uma chave para a [tabela binária](binary-table.md). Não é possível mostrar uma imagem e um texto em um botão.

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Ajuda
</dt> <dd>

As cadeias de caracteres de ajuda usadas com o botão. O texto é opcional e é localizável. A cadeia de caracteres é dividida em duas partes separadas por um caractere ( \| ). A primeira parte da cadeia de caracteres é usada como texto de dica de ferramenta. Esse texto é mostrado por leitores de tela para controles que contêm uma imagem. A segunda parte é usada para a ajuda contextual, embora a ajuda contextual ainda não tenha sido implementada. O caractere separador é necessário mesmo se apenas um dos dois tipos de texto estiver presente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores inteiros de x, y, Width e Height estão nas unidades de [instalação](installer-units.md), não nas unidades de caixa de diálogo. Uma unidade de instalador é igual a um décimo da altura do tamanho de fonte MS Sans Serif de 10 pontos. As coordenadas para os controles são relativas ao mural.

As coordenadas dos botões são dadas em relação ao grupo. Se as coordenadas do grupo forem alteradas, os botões dentro do grupo permanecerão na mesma posição relativa entre si.

O conteúdo dos campos Value e Text são formatados pela função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) quando o controle é criado, portanto, eles podem conter qualquer expressão que a função **MsiFormatRecord** possa interpretar. A formatação ocorre somente quando o controle é criado e não é atualizada se uma propriedade envolvida na expressão é modificada durante a vida útil do controle.

Cada controle de botão de opção é associado a uma propriedade. O valor padrão para essa propriedade deve ser inicializado na [tabela de propriedades](property-table.md). Em cada um dos botões de opção especificados na tabela RadioButton, pode haver um botão de opção com um valor no campo Value que corresponde ao valor padrão dessa propriedade. Este é o botão padrão para o controle de botão de opção. O botão padrão é mostrado inicialmente como selecionado no controle.

Observe que o usuário não pode alterar o foco em uma caixa de diálogo pressionando a tecla TAB para um controle de botão de opção até que um dos botões no grupo tenha sido selecionado. Para fazer com que o foco se mova para esse grupo de botões pressionando a tecla TAB, especifique um dos botões como um botão padrão para o grupo.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE34](ice34.md)  
[ICE46](ice46.md)  
</dl>

 

 



