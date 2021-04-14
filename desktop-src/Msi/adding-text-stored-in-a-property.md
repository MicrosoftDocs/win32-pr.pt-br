---
description: O exemplo descrito na seção intitulada criação de um &condicional \# 0034; Aguarde.
ms.assetid: b563e306-6d10-4298-9a71-9e749224ccd2
title: Adicionando texto armazenado em uma propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d43910b946db737d2b306d7c75f6683401eee0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370697"
---
# <a name="adding-text-stored-in-a-property"></a>Adicionando texto armazenado em uma propriedade

O exemplo descrito na seção intitulada [criação de uma condicional "Aguarde... "Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md) exibe uma caixa de diálogo com texto que lê:" Aguarde enquanto o custo do espaço em disco é concluído ". Isso pode ser feito simplesmente colocando um [controle de texto](text-control.md) na caixa de diálogo e inserindo a cadeia de texto na coluna de texto da [tabela de controle](control-table.md). Nesse caso, as informações sobre o estilo da fonte devem ser inseridas na cadeia de caracteres. O autor deve definir a fonte e o estilo da fonte ao prefixar a cadeia de caracteres com { \\ *Style*}. Em que *Style* é um identificador de estilo de fonte listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Esse método de adição de texto é ilustrado várias vezes em [um exemplo de instalação](an-installation-example.md).

Um autor de uma interface do usuário também pode armazenar texto em uma propriedade. O exemplo a seguir ilustra isso e mostra como ControlEvents pode ser usado para exibir cadeias de caracteres de texto alternativo.

O objetivo neste exemplo é inserir uma caixa de diálogo **WaitForCosting** enquanto uma tarefa em segundo plano está em execução. A diferença com o novo cenário é que, se o usuário cancelar a caixa de diálogo **WaitForCosting** e tentar ativar o controle antes que a tarefa em segundo plano tenha sido concluída uma segunda vez, a caixa **WaitForCosting** reaparecerá exibindo uma mensagem alternativa: "o custo do espaço em disco ainda está em execução. Você pode continuar aguardando ou retornando para a caixa de seleção principal para sair desta sequência. "

**Para exibir uma caixa de diálogo "Aguarde" que exibe mensagens alternativas**

1.  Comece adicionando uma caixa de diálogo **WaitForCosting** condicional a uma caixa de diálogo de seleção, conforme descrito em [criando uma condicional "Aguarde... "Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md).
2.  Coloque um [controle de texto](text-control.md) na caixa de diálogo **WaitForCosting** criando um registro na tabela de [controle](control-table.md). Insira o identificador da caixa de diálogo **WaitForCosting** na coluna de diálogo \_ . Insira o identificador do controle de texto na coluna de controle. Especifique o tipo de controle como texto na coluna tipo.
3.  Especifique o [atributo de controle de posição](position-control-attribute.md) para o controle de texto inserindo as coordenadas horizontal e vertical do canto superior esquerdo do controle nas colunas X e Y da [tabela de controle](control-table.md). Use pixels como unidades de distância.
4.  Especifique a largura e a altura do controle de texto inserindo essas dimensões nas colunas largura e altura da [tabela de controle](control-table.md). Use pixels como unidades de comprimento.
5.  A propriedade e o controle as \_ próximas colunas da tabela de controle não afetam os controles de texto e podem ser deixados em branco nesse caso.
6.  Especifique os atributos de controle para o controle de texto que estão associados aos sinalizadores de bit. Adicione os valores de bit individuais juntos e insira o total na coluna atributos da tabela de controle. Esses são os atributos de controle [Visible](visible-control-attribute.md), [relevo](sunken-control-attribute.md), [habilitado](enabled-control-attribute.md), [transparente](transparent-control-attribute.md), [nowrap](nowrap-control-attribute.md)e [NoPrefix](noprefix-control-attribute.md) . A combinação de bits que exibe um controle de texto em um plano de fundo opaco, com quebra de texto é 0, portanto, digite 0 ou deixe a coluna atributos em branco.
7.  A coluna de texto da tabela de controle pode ser deixada em branco. O controle de texto exibe a cadeia de texto que é o valor do atributo de controle de [texto](text-control-attribute.md) . O método para definir esse atributo é descrito nas etapas subsequentes deste procedimento.
8.  Adicione um registro na [tabela de propriedades](property-table.md) para definir a propriedade de mensagem FirstMessage. Essa propriedade é uma cadeia de caracteres que contém o estilo e o texto da fonte da primeira mensagem. Insira o nome FirstMessage na coluna propriedade. Na coluna valor, insira a cadeia de caracteres: "{ \\ waitstyle} aguarde enquanto o custo do espaço em disco é concluído". Em que Waitstyle é um identificador para um dos estilos de fonte listados na coluna TextStyle da [tabela TextStyle](textstyle-table.md).
9.  Adicione um registro na [tabela de propriedades](property-table.md) para definir a propriedade de mensagem SecondMessage. Essa propriedade é uma cadeia de caracteres que contém o estilo e o texto da fonte da segunda mensagem. Insira o nome SecondMessage na coluna propriedade. Na coluna valor, insira a cadeia de caracteres: "{ \\ waitstyle} o custo de espaço em disco ainda está em execução. Você pode continuar aguardando ou retornando para a caixa de seleção principal para sair desta sequência. "
10. Adicione um registro na [tabela de propriedades](property-table.md) para definir a propriedade de mensagem WaitMessage. Essa propriedade é uma cadeia de caracteres que contém o estilo e o texto da fonte para a mensagem exibida na caixa de diálogo **WaitForCosting** se o usuário tentar ativar um botão de ação antes de o custo ser concluído. Insira o nome WaitMessage na coluna propriedade. Na coluna valor da tabela de propriedades, digite: FirstMessage.
11. Adicione um [ControlEvent, SetProperty](setproperty-controlevent.md) à [tabela ControlEvent,](controlevent-table.md) que inicializa WaitMessage para FirstMessage sempre que uma nova caixa de diálogo de **seleção** é aberta. Insira o identificador para a caixa de diálogo que vem logo antes da caixa de diálogo de seleção na seqüência de caixas de diálogo na coluna de diálogo \_ . Insira o identificador para o controle nessa caixa de diálogo usada para abrir a caixa de diálogo de seleção na \_ coluna de controle. Insira \[ WaitMessage \] na coluna evento. Insira \[ FirstMessage \] na coluna argumento. Insira 1 na coluna condição e deixe a coluna ordem em branco.
12. Adicione um [ControlEvent, SetProperty](setproperty-controlevent.md) à [tabela ControlEvent,](controlevent-table.md) que define WaitMessage como SecondMessage se o usuário fechar a caixa de diálogo **WaitForCosting** antes que o custo de espaço em disco seja concluído. Insira o identificador para a caixa de diálogo **WaitForCosting** na coluna de diálogo \_ . Insira o identificador para o controle de texto na coluna de controle \_ . Insira \[ WaitMessage \] na coluna evento. Insira \[ SecondMessage \] na coluna argumento. Insira não [**CostingComplete**](costingcomplete.md) na coluna condição e deixe a coluna ordem em branco.
13. A etapa a seguir vincula o atributo de controle de texto ao ControlEvent, que gera a caixa de diálogo **WaitForCosting** . Isso faz com que o instalador passe o valor da propriedade WaitMessage para o atributo de controle de texto toda vez que o usuário abrir uma caixa de diálogo **WaitForCosting** .
14. Assine o atributo de controle de texto do controle de texto para o [SpawnWaitDialog ControlEvent,](spawnwaitdialog-controlevent.md) que abre a caixa de diálogo **WaitForCosting** adicionando um registro à [tabela EventMappings](eventmapping-table.md). Insira o identificador para a caixa de diálogo **WaitForCosting** na coluna de diálogo \_ . Insira o identificador para o controle de texto na coluna de controle \_ . Insira SpawnWaitDialog na coluna evento. Insira o texto, o identificador do atributo de controle de texto, na coluna atributo da tabela EventMappings.

 

 



