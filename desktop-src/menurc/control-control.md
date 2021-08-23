---
title: Controle de controle
description: Define um controle definido pelo usuário.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menus de controle de controle e outros recursos
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069449b5eef83cef7b7bdfac1c61aacb0ceac97cbbdd6e6fb2c139c43b3bae13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663056"
---
# <a name="control-control"></a>Controle de controle

Define um controle definido pelo usuário.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*classes*
</dt> <dd>

Nome redefinido, Cadeia de caracteres ou um valor inteiro sem sinal de 16 bits que define a classe. Pode ser qualquer uma das classes de controle; para obter uma lista das classes de controle, consulte a primeira lista após esta descrição. Se o valor for um nome redefinido fornecido pelo aplicativo, ele deverá ser uma cadeia de caracteres entre aspas duplas (").

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Nome redefinido ou valor inteiro que especifica o estilo do controle fornecido. O significado exato do *estilo* depende do valor da *classe* . As seções que seguem esta descrição mostram as classes de controle e os estilos correspondentes.

</dd> </dl>

Para obter mais informações sobre a sintaxe geral de uma instrução de controle, consulte [parâmetros de controle comuns](common-control-parameters.md).

## <a name="remarks"></a>Comentários

As seis classes de controle possíveis são descritas nas seções a seguir.

### <a name="the-button-control-class"></a>A classe de controle Button

Um controle de botão é uma pequena janela filho retangular que o usuário pode ativar ou desativar clicando com o mouse. Os controles de botão podem ser usados sozinhos ou em grupos e podem ser rotulados ou exibidos sem texto. Controles de botão normalmente alteram a aparência quando o usuário clica neles.

Os estilos de botão são descritos no tópico a seguir: [estilos de botão](../controls/button-styles.md).

### <a name="the-combo-box-control-class"></a>A classe de controle da caixa de combinação

Os controles de caixa de combinação consistem em um campo de seleção semelhante a um controle de edição, além de uma caixa de listagem. A caixa de listagem pode ser exibida sempre ou pode ser descartada quando o usuário seleciona uma "caixa pop" ao lado do campo de seleção.

Dependendo do estilo da caixa de combinação, o usuário pode ou não editar o conteúdo do campo de seleção. Se a caixa de listagem estiver visível, a digitação de caracteres na caixa de seleção fará com que a primeira entrada que corresponde aos caracteres digitados seja realçada. Por outro lado, a seleção de um item na caixa de listagem exibe o texto selecionado no campo seleção.

Os estilos de controle de caixa de combinação são descritos no seguinte tópico: [estilos de caixa de combinação](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>A classe de controle de edição

Um controle de edição é uma janela filho retangular na qual o usuário pode inserir texto do teclado. O usuário seleciona o controle e dá a ele o foco de entrada, clicando no mouse dentro dele ou pressionando a tecla TAB. O usuário pode inserir texto quando o controle exibe um ponto de inserção piscando. O mouse pode ser usado para mover o cursor e selecionar os caracteres a serem substituídos ou para posicionar o cursor para inserir caracteres. A tecla backspace pode ser usada para excluir caracteres.

Os controles de edição usam a fonte de densidade fixa e exibem caracteres Unicode. Eles expandem caracteres de tabulação em tantos caracteres de espaço quantos forem necessários para mover o cursor para a próxima parada de tabulação. As paradas de tabulação são consideradas em cada oitavo posição de caractere.

Os estilos de controle de edição são descritos no tópico a seguir: [Editar estilos de controle](../controls/edit-control-styles.md).

### <a name="the-list-box-control-class"></a>A classe de controle da caixa de listagem

Os controles de caixa de listagem consistem em uma lista de cadeias de caracteres. O controle é usado sempre que um aplicativo precisa apresentar uma lista de nomes, como nomes de File, que o usuário pode exibir e selecionar. O usuário pode selecionar uma cadeia de caracteres apontando para a cadeia de caracteres com o mouse e clicando em um botão do mouse. Quando uma cadeia de caracteres é selecionada, ela é realçada e uma mensagem de notificação é passada para a janela pai. Uma barra de rolagem pode ser usada com um controle de caixa de listagem para rolar listas que são muito longas ou muito amplas para a janela de controle.

Os estilos de controle de caixa de listagem são descritos no seguinte tópico: [estilos de caixa de listagem](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>A classe de controle Scroll-Bar

Um controle de barra de rolagem é um retângulo que contém um Thumb de rolagem e tem setas de direção em ambas as extremidades. A barra de rolagem envia uma mensagem de notificação para seu pai sempre que o usuário clica no controle. O pai é responsável por atualizar a posição do Thumb, se necessário. Os controles de barra de rolagem têm a mesma aparência e função que as barras de rolagem usadas em janelas comuns. Mas, ao contrário das barras de rolagem, os controles de barra de rolagem podem ser posicionados em qualquer lugar em uma janela e usados sempre que necessário para fornecer a entrada de rolagem para uma janela.

Os estilos da barra de rolagem são descritos no seguinte tópico: [estilos de controle da barra de rolagem](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>A classe de controle estático

Os controles estáticos são campos de texto simples, caixas e retângulos que podem ser usados para rotular, caixar ou separar outros controles. Os controles estáticos não utilizam nenhuma entrada e não fornecem nenhuma saída.

Os estilos de controle estáticos são descritos no seguinte tópico: [estilos de controle estático](../controls/static-control-styles.md).

 

 