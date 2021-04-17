---
description: O controle MaskedEdit é um controle de campo de edição que contém uma máscara no campo de texto do controle. Você pode associar o controle com uma propriedade de valor de cadeia de caracteres inserindo o nome da propriedade na coluna propriedade da tabela de controle.
ms.assetid: 8cc14683-3dbb-404f-87af-09a5f5b90b19
title: Controle MaskedEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7568df9969ebabab6311e519d0a5a625feb8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789772"
---
# <a name="maskededit-control"></a>Controle MaskedEdit

O controle MaskedEdit é um controle de campo de edição que contém uma máscara no campo de texto do controle. Você pode associar o controle com uma propriedade de valor de cadeia de caracteres inserindo o nome da propriedade na coluna propriedade da [tabela de controle](control-table.md).

Você pode usar o controle MaskedEdit para criar um modelo para entrada de usuário de informações, como um número de telefone ou código de ID de produto. Por exemplo, a propriedade [**PIDKEY**](pidkey.md) pode ser inserida pelo usuário por meio de um controle MaskedEdit que é especificado pela definição da propriedade [**PIDTemplate**](pidtemplate.md) para uma cadeia de caracteres como a seguinte:

12345<\#\#\# -%%%%%%%>@@@@@

A cadeia de caracteres define o modelo de mascaramento para a entrada da propriedade [**PIDKEY**](pidkey.md) pelo usuário. O segmento visível da cadeia de caracteres é colocado entre um par de caracteres de colchete (<>).

A tabela a seguir identificou a sintaxe da máscara.



| Caractere | Significado                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <      | A extremidade esquerda do segmento visível do modelo. Esse caractere e tudo para a esquerda ficam ocultos na interface do usuário. Não deve haver mais de uma instância desse caractere no modelo.                                                                               |
| >      | A extremidade direita do segmento visível do modelo. Esse caractere e tudo o que está à direita ficam ocultos na interface do usuário. Esse caractere é substituído por um traço durante a validação. Se houver um segmento visível começa com <, ele deve ser encerrado com um > correspondente. |
| \#        | Esse caractere pode ser um dígito (numeral).                                                                                                                                                                                                                                                    |
| %         | Esse caractere pode ser um dígito alternativo (numeral) que permite que a máscara controle a maneira como uma ação personalizada diferencia campos.                                                                                                                                                          |
| @         | Esse caractere pode ser um dígito aleatório (numeral). Esse caractere não deve aparecer na parte visível do modelo.                                                                                                                                                                       |
| &         | Esse caractere pode ser qualquer caractere.                                                                                                                                                                                                                                                        |
| ^         | Esse caractere pode ser um caractere alternativo que permite que a máscara controle a maneira como uma ação personalizada diferencia campos.                                                                                                                                                                |
| ?         | Esse caractere pode ser um caractere alternativo que permite que a máscara controle a maneira como uma ação personalizada diferencia campos.                                                                                                                                                                |
| \`        | Acento grave \` (valor ASCII 96) pode representar um caractere alternativo que permite que a máscara controle a maneira como uma ação personalizada diferencia campos.                                                                                                                                 |
| \_        | Esse caractere é um caractere de sublinhado literal.                                                                                                                                                                                                                                           |
| =         | Esse caractere é o terminador de campo. Isso deve seguir um \# ,%, ^ ou \` . Isso cria mais uma posição de entrada do mesmo tipo que as posições anteriores e encerra o campo com um separador '-'.                                                                                 |



 

Qualquer outro caractere é tratado como uma constante literal.

Para caracteres que podem ser editados, o controle cria janelas de edição separadas com uma janela para cada bloco de caracteres contíguos do mesmo tipo.

## <a name="control-attributes"></a>Atributos de controle

Para alterar o valor de um atributo que está usando um evento, assine o controle para um evento de controle na [tabela EventMappings](eventmapping-table.md) e liste o identificador de atributo na coluna atributo. Insira o identificador do evento de controle na coluna evento. Você pode usar os atributos a seguir com o controle MaskedEdit.



| Atributo                                                          | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Este é o nome de uma propriedade indireta que está associada ao controle. Se o bit de atributo indireto estiver definido, o controle exibirá ou alterará o valor da propriedade que tem esse nome. Se o bit de atributo indireto estiver definido, esse nome também será o valor da propriedade listada na coluna propriedade da tabela de [controle](control-table.md).                                                                                                                                   |
| [Posição](position-control-attribute.md)                         |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da tabela de [controle](control-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                                                                                                                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Este é o nome da propriedade associada a este controle. Se o bit de atributo indireto não estiver definido, o controle exibirá ou alterará o valor da propriedade que tem esse nome. Esse atributo é especificado na coluna propriedade da tabela de [controle](control-table.md).                                                                                                                                                                                                           |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor atual da propriedade que é exibida ou alterada por este controle. Se o bit de atributo indireto não estiver definido, esse será o valor de PropertyName. Se o bit de atributo indireto estiver definido, esse será o valor de IndirectPropertyName. Se o atributo for alterado, o controle refletirá o novo valor.                                                                                                                                                                                                |
| [Text](text-control-attribute.md)                                 |                                  | Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&Style}. Em que Style é um identificador listado na coluna Style da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. A cadeia de caracteres que especifica o modelo de mascaramento segue esse prefixo e usa a sintaxe descrita anteriormente neste tópico. |
| [Visível](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) para tornar o controle visível ou oculto quando ele for criado.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                 |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra de bits na coluna atributos da tabela de [controle](control-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                          |
| [Submersa](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                          |
| [Indireto.](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | O controle exibe ou altera o valor da propriedade na coluna propriedade da [tabela de controle](control-table.md). O controle exibe ou altera o valor da propriedade que tem o identificador listado na coluna propriedade da [tabela de controle](control-table.md).<br/> Determina se a propriedade associada a esse controle é referenciada indiretamente.<br/>                                                                                                 |



 

## <a name="remarks"></a>Comentários

O controle MaskedEdit cria uma janela pai da classe **Button** com os estilos **BS \_ OWNERDRAW** e **WS \_ ex \_ CONTROLPARENT** . Ele cria várias janelas filhas nessa janela.

-   Para partes de texto constantes, ele cria janelas estáticas com os estilos **\_ filho** **II e \_ esquerdo do SS** .
-   Para campos editáveis, ele cria uma janela de edição com os estilos **WS \_ filho**, **WS \_ Border** e **WS \_ TabStop** .
-   Para campos numéricos, a janela também tem o estilo de **\_ número es** .

Os campos dígito alternativo,%, e caracteres alfanuméricos alternativos, ^,?, e \` permitem que as ações personalizadas diferenciem os campos de uma maneira que possa ser controlada pela máscara, por exemplo, ^ pode ser usado para campos que devem estar em letras maiúsculas.

 

 




