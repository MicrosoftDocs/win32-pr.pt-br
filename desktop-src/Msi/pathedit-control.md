---
description: O controle PathEdit exibe um campo de edição que permite que um usuário selecione a seção final de um caminho.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: Controle PathEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed7655cc893c30f417c9a7ef374eb6d4ade10dfd618ca328e1be2fc7a0e0a9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377609"
---
# <a name="pathedit-control"></a>Controle PathEdit

O controle PathEdit exibe um campo de edição que permite que um usuário selecione a seção final de um caminho. Esse controle dá suporte à inserção do nome da pasta selecionada ou de todo o caminho no campo de edição. Um usuário também pode inserir um caminho UNC para uma unidade que não tem letra da unidade. Se o usuário inserir um segmento final para o caminho inválido para o volume atual, o controle PathEdit não poderá transferir o foco para o próximo controle.

Os controles PathEdit, [DirectoryCombo](directorycombo-control.md)e [DirectoryList](directorylist-control.md) estão associados à mesma propriedade com valor de cadeia de caracteres. Essa propriedade é o caminho selecionado pelo usuário. Insira o nome da propriedade na coluna Propriedade da [tabela Controle](control-table.md). Essa propriedade deve ter um valor inicial que contenha pelo menos um volume e um subnível. Especifique o valor inicial da propriedade na coluna Valor da [tabela Property](property-table.md).

Esse controle destina-se a ser usado em uma caixa de diálogo [Procurar](browse-dialog.md) junto com os controles PathEdit e [DirectoryList.](directorylist-control.md)

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com esse controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent na tabela [EventMapping](eventmapping-table.md) e liste o identificador do atributo na coluna Atributo. Insira o identificador do ControlEvent na coluna Evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Esse é o nome de uma propriedade indireta associada ao controle . Se o bit de atributo Indireto estiver definido, o controle exibirá ou altera o valor da propriedade que tem esse nome. Se o bit de atributo Indireto estiver definido, esse nome também será o valor da propriedade listada na coluna Propriedade da [tabela Controle](control-table.md).                                                                                                                                                                              |
| [Posição](position-control-attribute.md)                         |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do canto esquerdo do controle nas colunas Width, Height, X e Y da [tabela Control](control-table.md). Use [unidades do instalador](installer-units.md) para comprimento e distância.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Esse é o nome da propriedade associada a esse controle. Se o bit de atributo Indireto não estiver definido, o controle exibirá ou altera o valor da propriedade que tem esse nome. Esse atributo é especificado na coluna Propriedade da [tabela Control](control-table.md).                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor atual da propriedade exibida ou alterada por esse controle. Se o bit de atributo Indireto não estiver definido, esse será o valor de PropertyName. Se o bit de atributo Indireto estiver definido, esse será o valor de IndirectPropertyName. Se o atributo mudar, o controle refletirá o novo valor.                                                                                                                                                                                                                                 |
| [Text](text-control-attribute.md)                                 |                                  | Para definir o estilo de fonte e fonte de uma cadeia de caracteres de texto, prefixe a cadeia de caracteres exibida com { style} ou \\ {&style}. Em que style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhum deles estiver presente, mas a [**propriedade DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. Para especificar o número de caracteres que o usuário pode inserir, adeque {n} após qualquer especificação de fonte, em que n é um inteiro positivo.<br/> |
| [Visível](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra bit da coluna Atributos na tabela [Controle](control-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                           |
| [Habilitada](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra bit na coluna Atributos do [Controle](control-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                         |
| [Afundado](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com um esquente, 3D, look.<br/> Inclua esses bits na palavra bit na coluna Atributos da [tabela Controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indireto.](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | O controle exibe ou altera o valor da propriedade na coluna Propriedade da [tabela Controle](control-table.md). O controle exibe ou altera o valor da propriedade que tem o Identificador listado na coluna Propriedade da tabela Controle.<br/> Determina se a propriedade associada a esse controle é referenciada indiretamente.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | O texto no controle é exibido na ordem de leitura da esquerda para a direita. O texto no controle é exibido na ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle é alinhado à direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

O controle PathEdit é derivado do [controle](edit-control.md) Editar.

Para compatibilidade com os leitores de tela, ao fazer uma caixa de diálogo com um controle PathEdit como o primeiro controle ativo, você deve tornar o campo de texto pertencente ao campo de edição o primeiro controle ativo na tabela [Diálogo](dialog-table.md). Como o texto estático não pode se concentrar, quando a caixa de diálogo é criada, o campo de edição terá o foco inicialmente conforme o esperado; isso garante que os leitores de tela mostrem as informações corretas.

 

 




