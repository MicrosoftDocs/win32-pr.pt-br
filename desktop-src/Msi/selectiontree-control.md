---
description: Esse controle permite que um usuário altere o estado de seleção dos recursos listados na tabela de recursos.
ms.assetid: 0daf5b44-ba07-47f1-95d9-28c59f7cf985
title: Controle SelectionTree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5287736c3293c736d6d392ce8532b76ee7b62ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837298"
---
# <a name="selectiontree-control"></a>Controle SelectionTree

Esse controle permite que um usuário altere o estado de seleção dos recursos listados na [tabela de recursos](feature-table.md). O controle é associado a uma propriedade com valor de cadeia de caracteres que o usuário pode definir por uma [caixa de diálogo de procura](browse-dialog.md). Você pode associar o controle a uma propriedade inserindo o nome da propriedade na coluna propriedade da tabela de [controle](control-table.md).

O controle SelectionTree publica automaticamente os eventos de [controle](control-events.md) a seguir no Windows XP ou em sistemas operacionais anteriores. O controle SelectionTree publica esses eventos quando o item selecionado é alterado de um nó para outro. Se a árvore de seleção não tiver nós, o controle publicará esses eventos e apagará o conteúdo dos controles que assinam o evento. Esses ControlEvents não devem ser listados na [tabela ControlEvent,](controlevent-table.md).



| Evento de controle                                                 | Descrição                                                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Selectionaction](selectionaction-controlevent.md)           | Publica uma cadeia de caracteres da [tabela UIText](uitext-table.md) que descreve o item realçado.      |
| [SelectionBrowse](selectionbrowse-controlevent.md)           | Gera uma caixa de diálogo de procura usada para modificar o caminho do item realçado.                     |
| [SelectionDescription](selectiondescription-controlevent.md) | Publica uma cadeia de caracteres da [tabela de recursos](feature-table.md) que descreve o item realçado.    |
| [SelectionNoItems](selectionnoitems-controlevent.md)         | Exclui o texto descritivo ou desabilita os botões de um item obsoleto.                          |
| [SelectionPath](selectionpath-controlevent.md)               | Publica o caminho para o item realçado.                                                       |
| [SelectionPathOn](selectionpathon-controlevent.md)           | Publica se há um caminho de seleção associado ao recurso selecionado no momento. |
| [SelectionSize](selectionsize-controlevent.md)               | Publica o tamanho do item realçado.                                                        |



 

A partir dos sistemas Windows Server 2003, os controles SelectionTree publicam todos os eventos na tabela acima e, além disso, publicam um [ControlEvent, DoAction](doaction-controlevent.md) ou um [ControlEvent, SetProperty](setproperty-controlevent.md). Os registros devem ser adicionados à [tabela ControlEvent,](controlevent-table.md) para publicar DoAction ou SetProperty ControlEvents.



| Evento de controle                               | Descrição                                        |
|---------------------------------------------|----------------------------------------------------|
| [DoAction](doaction-controlevent.md)       | Notifica o instalador para executar uma ação personalizada. |
| [SetProperty](setproperty-controlevent.md) | Define uma propriedade para um novo valor.                    |



 

Começando com Windows Installer versão 3,0, os controles SelectionTree publicam um evento que executa [ações personalizadas](custom-actions.md) listadas na [tabela ControlEvent,](controlevent-table.md). O controle SelectionTree publica esse evento sempre que a seleção de recursos é alterada no controle ou sempre que um estado de seleção diferente é escolhido para o recurso atual. As ações personalizadas são executadas cada vez que o evento é publicado. O controle SelectionTree envia informações para a ação personalizada definindo os valores das propriedades a seguir. Todas essas propriedades são todas limpas quando o controle SelectionTree é fechado.

**Windows Installer 2,0:** Sem suporte. O controle SelectionTree não publica o evento e não define as propriedades a seguir.



| Propriedade                                | Descrição                                                                                                                                                      |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MsiSelectionTreeSelectedFeature         | O nome do recurso selecionado no campo recurso da tabela de [recursos](feature-table.md).                                                                      |
| MsiSelectionTreeSelectedAction          | O estado da ação de instalação do recurso selecionado. O valor pode ser INSTALLstate \_ ausente, InstallState \_ local, InstallState \_ Source ou InstallState \_ anunciado. |
| MsiSelectonTreeChildrenCount            | Número de nós filho diretos.                                                                                                                                    |
| MsiSelectionTreeInstallingChildrenCount | Número de nós filho diretos que são INSTALLstate \_ local, instalação de \_ origem ou InstallState \_ anunciado.                                                    |
| MsiSelectionTreeSelectedCost            | Custo da instalação do recurso selecionado em unidades de 512 bytes.                                                                                                   |
| MsiSelectionTreeChildrenCost            | Custo da instalação de todos os recursos filhos em unidades de 512 bytes.                                                                                              |
| MsiSelectionTreeSelectedPath            | Caminho em que o recurso selecionado está sendo instalado. Definido somente se o recurso estiver sendo instalado como INSTALLstate \_ local.                                       |



 

> [!Note]
>
> O conteúdo do campo de texto da [tabela de controle](control-table.md) nunca é exibido pelo controle SelectionTree. Em vez disso, esse campo especifica o estilo do texto a ser exibido pelo controle e contém uma descrição do controle usado pelos utilitários de revisão de tela. Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&*Style*}. Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada. As informações a seguir são lidas por utilitários de revisão de tela como a descrição do controle. Consulte [acessibilidade](accessibility.md).

 

## <a name="control-attributes"></a>Atributos de controle

Você pode usar os atributos a seguir com este controle. Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo. Insira o identificador do ControlEvent, na coluna de evento.



| Identificador de atributo                                               | Bit hexadecimal                  | Descrição                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nome de uma propriedade indireta associada ao controle. Se o bit de atributo indireto estiver definido, o controle exibirá ou alterará o valor da propriedade com esse nome. Se o bit de atributo indireto estiver definido, esse nome também será o valor da propriedade listada na coluna propriedade da [tabela de controle](control-table.md).                                    |
| [Posição](position-control-attribute.md)                         |                                  | Posição do controle na caixa de diálogo. Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da [tabela de controle](control-table.md). Use [unidades de instalador](installer-units.md) para duração e distância.<br/>                                                                             |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nome da propriedade associada a este controle. Se o bit de atributo indireto não estiver definido, o controle exibirá ou alterará o valor da propriedade com esse nome. Esse atributo é especificado na coluna propriedade da tabela de [controle](control-table.md).                                                                                                    |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valor atual da propriedade exibida ou alterada por este controle. Se o bit de atributo indireto não estiver definido, esse será o valor de PropertyName. Se o bit de atributo indireto estiver definido, esse será o valor de IndirectPropertyName. Se o atributo for alterado, o controle refletirá o novo valor.                                                                           |
| [Text](text-control-attribute.md)                                 |                                  | Exibe o texto em leitores de acordo com o texto inserido na coluna de texto da [tabela de controle](control-table.md). Consulte [acessibilidade](accessibility.md).                                                                                                                                                                                                          |
| [Visível](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controle oculto. Controle visível.<br/> Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) para tornar o controle visível ou oculto após sua criação.<br/> Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                     |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controle em um estado desabilitado. Controle em um estado habilitado.<br/> Inclua esse bit na palavra de bits na coluna atributos do [controle](control-table.md) para habilitar o controle na criação.<br/> Você também pode habilitar ou desabilitar um controle usando a [tabela ControlCondition](controlcondition-table.md).<br/>                                   |
| [Submersa](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Exibe o estilo visual padrão. Exibe o controle com uma aparência de baixo e baixo, 3D.<br/> Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).<br/>                                                                                                                                                             |
| [Indireto.](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | O controle exibe ou altera o valor da propriedade na coluna propriedade da [tabela de controle](control-table.md). O controle exibe ou altera o valor da propriedade que tem o identificador listado na coluna propriedade da tabela de controle.<br/> Determina se a propriedade associada a esse controle é referenciada indiretamente.<br/> |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | O texto no controle é exibido na ordem de leitura da esquerda para a direita. O texto no controle é exibido na ordem de leitura da direita para a esquerda.<br/>                                                                                                                                                                                                                              |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | O texto no controle é alinhado à esquerda. O texto no controle é alinhado à direita.<br/>                                                                                                                                                                                                                                                                       |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | A barra de rolagem está localizada no lado direito do controle. A barra de rolagem está localizada no lado esquerdo do controle.<br/>                                                                                                                                                                                                                                         |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | Defina esse valor para uma combinação dos atributos [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

Esse controle pode ser criado a partir da \_ classe TreeView WC usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Ele tem o **WS \_ Border**, **TVs \_ HASLINES**, **TVs \_ HASBUTTONS**, **TVs \_ LINESATROOT**, **TVs \_ DISABLEDRAGDROP**, **TVs \_ SHOWSELALWAYS**, **WS- \_ Child**, **WS \_ TabStop** e **WS \_ Group** Styles.

A árvore de seleção só será populada se a [ação CostInitialize](costinitialize-action.md) e a [ação CostFinalize](costfinalize-action.md) tiverem sido chamadas.

A cadeia de caracteres a seguir na [tabela UIText](uitext-table.md) está relacionada a este controle.



| Termo                                                                                                         | Descrição                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="AbsentPath"></span><span id="absentpath"></span><span id="ABSENTPATH"></span>AbsentPath<br/> | O caminho exibido para um item no estado ausente.<br/> |



 

As seis cadeias de caracteres a seguir são usadas para exibir o número de filhos selecionados e o tamanho associado ao item realçado:

-   SelChildCostPos
-   SelChildCostNeg
-   SelParentCostPosPos
-   SelParentCostPosNeg
-   SelParentCostNegPos
-   SelParentCostNegNeg

As seguintes cadeias de caracteres são usadas para exibir as opções de seleção disponíveis para um item em um menu pop-up:

-   MenuAbsent
-   MenuLocal
-   MenuCD
-   MenuNetwork
-   MenuAllLocal
-   MenuAllCD
-   MenuAllNetwork

As cadeias de caracteres a seguir são usadas para explicar a seleção atual no [SelectionDescription](selectiondescription-controlevent.md) ControlEvent,.

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

 

 
