---
description: O controle PathEdit exibe um campo de edição que permite que um usuário selecione a seção final de um caminho.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: Controle PathEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65d1237199f202e6c674ab4526ccd4747b02c09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169523"
---
# <a name="pathedit-control"></a>Controle PathEdit

O controle PathEdit exibe um campo de edição que permite que um usuário selecione a seção final de um caminho. Esse controle dá suporte à inserção do nome da pasta selecionada ou do caminho inteiro no campo editar. Um usuário também pode inserir um caminho UNC (Convenção de nomenclatura universal) para uma unidade que não tenha letra de unidade. Se o usuário inserir um segmento final para o caminho inválido para o volume atual, o controle PathEdit não poderá transferir o foco para o próximo controle.

Os controles PathEdit, [DirectoryCombo](directorycombo-control.md)e [directorylist](directorylist-control.md) são associados à mesma propriedade com valor de cadeia de caracteres. Essa propriedade é o caminho selecionado pelo usuário. Insira o nome da propriedade na coluna propriedade da tabela de [controle](control-table.md). Essa propriedade deve ter um valor inicial contendo pelo menos um único volume e um subnível. Especifique o valor inicial para a propriedade na coluna valor da tabela de [Propriedades](property-table.md).

Esse controle deve ser usado em uma caixa de [diálogo de navegação](browse-dialog.md) junto com os controles PathEdit e [directorylist](directorylist-control.md) .

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com este controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Este é o nome de uma propriedade indireta associada ao controle. Se o bit de atributo indireto estiver definido, o controle exibirá ou alterará o valor da propriedade com esse nome. Se o bit de atributo indireto estiver definido, esse nome também será o valor da propriedade listada na coluna propriedade da [tabela de controle](control-table.md).                                                                                                                                                                              |
| [Posição](position-control-attribute.md)                         |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da [tabela de controle](control-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Este é o nome da propriedade associada a este controle. Se o bit de atributo indireto não estiver definido, o controle exibirá ou alterará o valor da propriedade com esse nome. Esse atributo é especificado na coluna propriedade da tabela de [controle](control-table.md).                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor atual da propriedade exibida ou alterada por este controle. Se o bit de atributo indireto não estiver definido, esse será o valor de PropertyName. Se o bit de atributo indireto estiver definido, esse será o valor de IndirectPropertyName. Se o atributo for alterado, o controle refletirá o novo valor.                                                                                                                                                                                                                                 |
| [Text](text-control-attribute.md)                                 |                                  | Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&Style}. Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. Para especificar o número de caracteres que o usuário pode inserir, acrescente {n} após qualquer especificação de fonte, em que n é um inteiro positivo.<br/> |
| [Visível](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                           |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra de bits na coluna atributos do [controle](control-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                         |
| [Submersa](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e 3-D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indireto.](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | O controle exibe ou altera o valor da propriedade na coluna propriedade da [tabela de controle](control-table.md). O controle exibe ou altera o valor da propriedade que tem o identificador listado na coluna propriedade da tabela de controle.<br/> Determina se a propriedade associada a esse controle é referenciada indiretamente.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | O texto no controle é exibido na ordem de leitura da esquerda para a direita. O texto no controle é exibido na ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle é alinhado à direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

O controle PathEdit é derivado do controle de [edição](edit-control.md) .

Para compatibilidade com leitores de tela, ao criar uma caixa de diálogo com um controle PathEdit como o primeiro controle ativo, você deve tornar o campo de texto pertencente ao campo de edição o primeiro controle ativo na [tabela de diálogo](dialog-table.md). Como o texto estático não pode se concentrar, quando a caixa de diálogo é criada, o campo de edição terá o foco inicialmente como pretendido; Isso garante que os leitores de tela mostrem as informações corretas.

 

 




