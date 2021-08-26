---
description: Esse controle permite que um usuário altere o estado de seleção dos recursos listados na tabela Recurso.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: Controle SelectionTree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894a7d90829172c29a6f1df1ffc4139cc0bf6c540bd49193c3cc2f3a396891ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040346"
---
# <a name="selectiontree-control"></a>Controle SelectionTree

Esse controle permite que um usuário altere o estado de seleção dos recursos listados na [tabela Recurso](feature-table.md). O controle está associado a uma propriedade com valor de cadeia de caracteres que o usuário pode definir por uma [caixa de diálogo Procurar](browse-dialog.md). Você pode associar o controle a uma propriedade inserindo o nome da propriedade na coluna Propriedade da [tabela Controle](control-table.md).

O controle SelectionTree publica automaticamente os seguintes Eventos [de](control-events.md) Controle Windows XP ou sistemas operacionais anteriores. O controle SelectionTree publica esses eventos quando o item selecionado é alterado de um nó para outro. Se a árvore de seleção não tiver nós, o controle publicará esses eventos e apagará o conteúdo dos controles que assinam o evento. Esses ControlEvents não precisam ser listados na [tabela ControlEvent](controlevent-table.md).



| Evento de controle                                                 | Descrição                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [SelectionAction](selectionaction-controlevent.md)           | Publica uma cadeia de caracteres da [tabela UIText que](uitext-table.md) descreve o item realçado.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Gera uma caixa de diálogo Procurar usada para modificar o caminho do item realçado.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Publica uma cadeia de caracteres da [tabela Recurso](feature-table.md) que descreve o item realçado.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Exclui o texto descritivo ou desabilita os botões de um item obsoleto.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Publica o caminho para o item realçado.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Publica se há ou não um caminho de seleção associado ao recurso selecionado no momento. |
| [SelectionSize](selectionsize-controlevent.md)               | Publica o tamanho do item realçado.                                                        |



 

A partir dos sistemas Windows Server 2003, os controles SelectionTree publicam todos os eventos na tabela acima e, além disso, publicam um [DoAction ControlEvent](doaction-controlevent.md) ou [um SetProperty ControlEvent](setproperty-controlevent.md). Os registros devem ser adicionados à [tabela ControlEvent](controlevent-table.md) para publicar DoAction ou SetProperty ControlEvents.



| Evento de controle                               | Descrição                                        |
|---------------------------------------------|----------------------------------------------------|
| [Doaction](doaction-controlevent.md)       | Notifica o instalador para executar uma ação personalizada. |
| [SetProperty](setproperty-controlevent.md) | Define uma propriedade como um novo valor.                    |



 

Começando com Windows Installer versão 3.0, os controles [](custom-actions.md) SelectionTree publicam um evento que executa ações personalizadas listadas na [tabela ControlEvent](controlevent-table.md). O controle SelectionTree publica esse evento sempre que a seleção de recursos muda no controle ou sempre que um estado de seleção diferente é escolhido para o recurso atual. As ações personalizadas são executados sempre que o evento é publicado. O controle SelectionTree envia informações para a ação personalizada definindo os valores das propriedades a seguir. Todas essas propriedades são limpas quando o controle SelectionTree é fechado.

**Windows Instalador 2.0:** Sem suporte. O controle SelectionTree não publica o evento e não configura as propriedades a seguir.



| Propriedade                                | Descrição                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | O nome do recurso selecionado no campo Recurso da [tabela Recurso](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | O estado de ação de instalação do recurso selecionado. O valor pode ser INSTALLSTATE \_ ABSENT, INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE ou INSTALLSTATE \_ ADVERTISED. |
| MsiSelectonTreeChildrenCount            | Número de nós filho diretos.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Número de nós filho diretos que são INSTALLSTATE \_ LOCAL, INSTALLSTATE \_ SOURCE ou INSTALLSTATE \_ ADVERTISED.                                                    |
| MsiSelectionTreeSelectedCost            | Custo de instalação do recurso selecionado em unidades de 512 bytes.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Custo de instalação de todos os recursos filhos em unidades de 512 bytes.                                                                                              |
| MsiSelectionTreeSelectedPath            | Caminho em que o recurso selecionado está sendo instalado. Definido somente se o recurso estiver sendo instalado como INSTALLSTATE \_ LOCAL.                                       |



 

> [!Note]
>
> O conteúdo do campo Texto da tabela [Controle](control-table.md) nunca é exibido pelo controle SelectionTree. Em vez disso, esse campo especifica o estilo do texto a ser exibido pelo controle e contém uma descrição do controle usado pelos utilitários de revisão de tela. Para definir o estilo de fonte e fonte de uma cadeia de caracteres de texto, prefixe a cadeia de caracteres exibida com { style} ou \\ {&*style*}. Em que style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhum deles estiver presente, mas a [**propriedade DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. As informações a seguir são lidas pelos utilitários de revisão de tela como a descrição do controle. Consulte [Acessibilidade](accessibility.md).

 

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com esse controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent na tabela [EventMapping](eventmapping-table.md) e liste o identificador do atributo na coluna Atributo. Insira o identificador do ControlEvent na coluna Evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nome de uma propriedade indireta associada ao controle . Se o bit de atributo Indireto estiver definido, o controle exibirá ou altera o valor da propriedade que tem esse nome. Se o bit de atributo Indireto estiver definido, esse nome também será o valor da propriedade listada na coluna Propriedade da [tabela Controle](control-table.md).                                    |
| [Posição](position-control-attribute.md)                         |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do canto esquerdo do controle nas colunas Width, Height, X e Y da [tabela Control](control-table.md). Use [unidades do instalador](installer-units.md) para comprimento e distância.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nome da propriedade associada a esse controle. Se o bit de atributo Indireto não estiver definido, o controle exibirá ou altera o valor da propriedade que tem esse nome. Esse atributo é especificado na coluna Propriedade da [tabela Control](control-table.md).                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor atual da propriedade exibida ou alterada por esse controle. Se o bit de atributo Indireto não estiver definido, esse será o valor de PropertyName. Se o bit de atributo Indireto estiver definido, esse será o valor de IndirectPropertyName. Se o atributo mudar, o controle refletirá o novo valor.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Exibe texto em screenreaders de acordo com o texto inserido na coluna Texto da [tabela Controle](control-table.md). Consulte [Acessibilidade](accessibility.md).                                                                                                                                                                                                          |
| [Visível](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra bit da coluna Atributos na tabela [Controle](control-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                     |
| [Habilitada](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra bit na coluna Atributos do [Controle](control-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                   |
| [Afundado](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com um esquente, 3D, look.<br/> Inclua esses bits na palavra bit na coluna Atributos da [tabela Controle](control-table.md).<br/>                                                                                                                                                             |
| [Indireto.](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | O controle exibe ou altera o valor da propriedade na coluna Propriedade da [tabela Controle](control-table.md). O controle exibe ou altera o valor da propriedade que tem o Identificador listado na coluna Propriedade da tabela Controle.<br/> Determina se a propriedade associada a esse controle é referenciada indiretamente.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | O texto no controle é exibido na ordem de leitura da esquerda para a direita. O texto no controle é exibido na ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle é alinhado à direita.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | A barra de rolagem está localizada no lado direito do controle. A barra de rolagem está localizada no lado esquerdo do controle.<br/>                                                                                                                                                                                                                                         |
| [Bidi](bidi-control-attribute.md)                                 | 0x000000E0                       | De definir esse valor para uma combinação dos atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll.](leftscroll-control-attribute.md)                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da classe WC \_ TREEVIEW usando a [**função CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Ele tem os estilos **WS \_ BORDER**, **TVS \_ HASLINES,** **TVS \_ HASBUTTONS,** **TVS \_ LINESATROOT,** **TVS \_ DISABLEDRAGDROP,** **TVS \_ SHOWSELALWAYS,** **WS \_ CHILD,** **WS \_ TABSTOP** e **WS \_ GROUP.**

A árvore de seleção só será populada se a [ação CostInitialize](costinitialize-action.md) e [a ação CostFinalize](costfinalize-action.md) foram chamadas.

A cadeia de caracteres a seguir [na tabela UIText](uitext-table.md) está relacionada a esse controle.



| Termo                                                                                                         | Descrição                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | O caminho exibido para um item no estado ausente.<br/> |



 

As seis cadeias de caracteres a seguir são usadas para exibir o número de filhos selecionados e o tamanho associado ao item realçado:

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNegNeg

As seguintes cadeias de caracteres são usadas para exibir as opções de seleção disponíveis para um item em um menu pop-up:

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

As cadeias de caracteres a seguir são usadas para explicar a seleção presente no [SelectionDescription](selectiondescription-controlevent.md) ControlEvent.

-   SelAbsentAbsent
-   SelAbsentLocal
-   SelAbsentCD
-   SelAbsentNetwork
-   SelLocalAbsent
-   SelLocalLocal
-   SelLocalCD
-   SelLocalNetwork
-   SelCDAbsent
-   SelNetworkAbsent
-   SelCDLocal
-   SelNetworkLocal
-   SelCDCD
-   SelNetworkNetwork

As quatro cadeias de caracteres localizadas a seguir são usadas para formatar o tamanho de um arquivo:

-   Bytes
-   KB
-   MB
-   GB

 

 
