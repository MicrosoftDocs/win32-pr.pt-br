---
description: Um controle Directorylist exibe uma parte do caminho que é atualmente exibido no controle PathEdit. O controle Directorylist exibe as pastas abaixo do diretório exibido atualmente pelo controle DirectoryCombo.
ms.assetid: 05e70381-28c0-4568-808e-ff2dee8ff790
title: Controle directorylist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6a1e48a25ae057c836c7b815dae18e7dcf5c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764660"
---
# <a name="directorylist-control"></a>Controle directorylist

Um controle Directorylist exibe uma parte do caminho que é atualmente exibido no [controle PathEdit](pathedit-control.md). O controle Directorylist exibe as pastas abaixo do diretório exibido atualmente pelo [controle DirectoryCombo](directorycombo-control.md).

Os controles PathEdit, DirectoryCombo e Directorylist são associados à mesma propriedade com valor de cadeia de caracteres. Essa propriedade é o caminho selecionado pelo usuário. Insira o nome da propriedade na coluna propriedade da tabela de [controle](control-table.md). Essa propriedade deve ter um valor inicial contendo pelo menos um volume e um subnível. Especifique o valor inicial para a propriedade na coluna valor da tabela de [Propriedades](property-table.md).

Esse controle deve ser usado em uma caixa de [diálogo de navegação](browse-dialog.md) junto com o controle [PathEdit](pathedit-control.md) e directorylist.

O controle Directorylist publica o seguinte ControlEvents.



| ControlEvent                                            | Descrição                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| [DirectoryListNew](directorylistnew-controlevent.md)   | Cria uma nova pasta e seleciona o campo nome para edição.      |
| [IgnoreChange](ignorechange-controlevent.md)           | Realça, mas não abre, uma pasta no diretório atual. |
| [DirectoryListUp](directorylistup-controlevent.md)     | Seleciona o pai do diretório atual.                      |
| [DirectoryListOpen](directorylistopen-controlevent.md) | Seleciona e realça um diretório.                               |



 

O conteúdo do campo de texto da [tabela de controle](control-table.md) nunca é exibido pelo controle directorylist. Em vez disso, esse campo especifica o estilo do texto a ser exibido pelo controle e contém uma descrição do controle usado pelos utilitários de revisão de tela. Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&*Style*}. Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. As informações a seguir são lidas por utilitários de revisão de tela como a descrição do controle. Consulte [acessibilidade](accessibility.md).

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com este controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Este é o nome de uma propriedade indireta associada ao controle. Se o bit de atributo indireto estiver definido, o controle exibirá ou alterará o valor da propriedade com esse nome. Se o bit de atributo indireto estiver definido, esse nome também será o valor da propriedade listada na coluna propriedade da [tabela de controle](control-table.md).                        |
| [Posição](position-control-attribute.md)                         |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da [tabela de controle](control-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Este é o nome da propriedade associada a este controle. Se o bit de atributo indireto não estiver definido, o controle exibirá ou alterará o valor da propriedade com esse nome. Esse atributo é especificado na coluna propriedade da tabela de [controle](control-table.md).                                                                                        |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor atual da propriedade exibida ou alterada por este controle. Se o bit de atributo indireto não estiver definido, esse será o valor de PropertyName. Se o bit de atributo indireto estiver definido, esse será o valor de IndirectPropertyName. Se o atributo for alterado, o controle refletirá o novo valor.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Para exibir o texto em leitores de tela, insira o texto na coluna texto da [tabela de controle](control-table.md). Consulte [acessibilidade](accessibility.md).                                                                                                                                                                                                                 |
| [Visível](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md). para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra de bits na coluna atributos do [controle](control-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                   |
| [Submersa](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e baixo, 3D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                             |
| [Indireto.](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | O controle exibe ou altera o valor da propriedade na coluna propriedade da [tabela de controle](control-table.md). O controle exibe ou altera o valor da propriedade que tem o identificador listado na coluna propriedade da tabela de controle.<br/> Determina se a propriedade associada a esse controle é referenciada indiretamente.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | O texto no controle é exibido na ordem de leitura da esquerda para a direita. O texto no controle é exibido na ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle é alinhado à direita.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | A barra de rolagem está localizada no lado direito do controle. A barra de rolagem está localizada no lado esquerdo do controle.<br/>                                                                                                                                                                                                                                         |
| [Controle BiDi](bidi-control-attribute.md)                         | 0x000000E0                       | Defina esse valor para uma combinação dos atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da \_ classe WC ListView usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem os **estilos \_ lista de LVS**, **LVS \_ EDITLABELS**, **WS \_ VSCROLL**, **LVS \_ SHAREIMAGELISTS**, **LVS \_ autoorganize**, **LVS \_ SINGLESEL**, **WS \_ Border**, **LVS \_ SORTASCENDING**, **WS \_ filho**, **WS \_ Group** e **WS \_ TabStop** .

Esse controle permite que o usuário selecione uma subpasta da seleção atual. Com botões adicionais, ele também permite que o usuário selecione uma nova pasta na seleção atual ou percorra um nível no caminho. Se o usuário escolher o botão **criar nova pasta** em uma pasta em que uma nova pasta já existe, uma segunda pasta não será criada e o nome da nova pasta existente será selecionado para edição.

 

