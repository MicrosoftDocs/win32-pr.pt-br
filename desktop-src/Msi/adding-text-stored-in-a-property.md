---
description: O exemplo descrito na seção intitulada Authoring a Conditional &\# 0034; Aguarde.
ms.assetid: b563e306-6d10-4298-9a71-9e749224ccd2
title: Adicionando texto armazenado em uma propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 965a90c5e0701c54959bb4eae26b26c07ad7b4cbae8aefa6bdf346542b6a5cf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105446"
---
# <a name="adding-text-stored-in-a-property"></a>Adicionando texto armazenado em uma propriedade

O exemplo descrito na seção intitulada [Authoring a Conditional "Please Wait . . " Caixa de Mensagem](authoring-a-conditional-please-wait-------message-box.md) exibe uma caixa de diálogo com texto que diz: "Aguarde enquanto o custo do espaço em disco é concluído". Isso pode ser feito simplesmente colocando um Controle de [Texto](text-control.md) na caixa de diálogo e inserindo a cadeia de caracteres de texto na coluna Texto da [tabela Controle](control-table.md). Nesse caso, as informações sobre o estilo da fonte devem ser inseridas na cadeia de caracteres. O autor deve definir o estilo de fonte e fonte prefixando a cadeia de caracteres com { \\ *style*}. Em *que style* é um identificador de estilo de fonte listado na coluna TextStyle da tabela [TextStyle](textstyle-table.md). Esse método de adição de texto é ilustrado várias vezes em [Um exemplo de instalação](an-installation-example.md).

Um autor de uma interface do usuário também pode armazenar texto em uma propriedade. O exemplo a seguir ilustra isso e mostra como ControlEvents pode ser usado para exibir cadeias de caracteres de texto alternativas.

O objetivo neste exemplo é novamente colocar uma caixa de **diálogo WaitForCosting** enquanto uma tarefa em segundo plano está em execução. A diferença com o novo cenário é que, se o usuário cancelar a caixa de diálogo **WaitForCosting** e tentar ativar o controle antes que a tarefa em segundo plano seja concluída uma segunda vez, a caixa **WaitForCosting** reaparece exibindo uma mensagem alternativa: "O custo do espaço em disco ainda está em execução. Você pode continuar a aguardar ou retornar à caixa de seleção principal para sair dessa sequência."

**Para exibir uma caixa de diálogo "Aguarde" que exibe mensagens alternativas**

1.  Comece adicionando uma caixa de **diálogo WaitForCosting** condicional a uma caixa de diálogo Seleção, conforme descrito em [Authoring a Conditional "Please Wait . . . " Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md).
2.  Coloque um [controle de](text-control.md) texto na caixa de **diálogo WaitForCosting,** com a publicação de um registro na [tabela Controle](control-table.md). Insira o identificador da caixa **de diálogo WaitForCosting** na coluna \_ Diálogo. Insira o identificador do controle Texto na coluna Controle. Especifique o tipo de controle como Texto na coluna Tipo.
3.  [Especifique](position-control-attribute.md) o atributo de controle Posição para o controle de texto inserindo as coordenadas horizontais e verticais do canto superior esquerdo do controle nas colunas X e Y da [tabela Controle](control-table.md). Use pixels como unidades de distância.
4.  Especifique a largura e a altura do controle de texto inserindo essas dimensões nas colunas Largura e Altura da [tabela Controle](control-table.md). Use pixels como unidades de comprimento.
5.  As colunas Property e Control Next da tabela Control não afetam os controles Text e podem \_ ser deixadas em branco nesse caso.
6.  Especifique os atributos de controle para o controle Texto associados aos sinalizadores de bits. Adicione os valores de bit individuais e insira o total na coluna Atributos da tabela Controle. Esses são os [atributos de](visible-control-attribute.md)controle Visible , [Sunken](sunken-control-attribute.md), [Enabled,](enabled-control-attribute.md) [Transparent,](transparent-control-attribute.md) [NoWrap](nowrap-control-attribute.md)e [NoPrefix.](noprefix-control-attribute.md) A combinação de bits que exibem um controle de texto em uma tela de fundo opaca, com o texto de quebra é 0, portanto, insira 0 ou deixe a coluna Atributos em branco.
7.  A coluna Texto da tabela Controle pode ser deixada em branco. O controle Texto exibe a cadeia de caracteres de texto que é o valor do [atributo Controle](text-control-attribute.md) de texto. O método para definir esse atributo é descrito nas etapas subsequentes deste procedimento.
8.  Adicione um registro na tabela [Property para](property-table.md) definir a propriedade de mensagem FirstMessage. Essa propriedade é uma cadeia de caracteres que contém o estilo de fonte e o texto da primeira mensagem. Insira o nome FirstMessage na coluna Propriedade. Na coluna Valor, insira a cadeia de caracteres: "{ WaitStyle}Aguarde enquanto o custo do espaço em disco \\ é concluído." Em que WaitStyle é um identificador para um dos estilos de fonte listados na coluna TextStyle da [tabela TextStyle](textstyle-table.md).
9.  Adicione um registro na tabela [Property para](property-table.md) definir a propriedade secondMessage message. Essa propriedade é uma cadeia de caracteres que contém o estilo de fonte e o texto da segunda mensagem. Insira o nome SecondMessage na coluna Propriedade. Na coluna Valor, insira a cadeia de caracteres: "{ WaitStyle}O custo do espaço \\ em disco ainda está em execução. Você pode continuar a aguardar ou retornar à caixa de seleção principal para sair dessa sequência."
10. Adicione um registro na tabela [Property para](property-table.md) definir a propriedade de mensagem WaitMessage. Essa propriedade é uma cadeia de caracteres que contém o estilo de fonte e o texto da mensagem exibida na caixa de **diálogo WaitForCosting** se o usuário tentar ativar um botão de push antes que o custo seja concluído. Insira o nome WaitMessage na coluna Propriedade. Na coluna Valor da tabela Propriedade, insira: FirstMessage.
11. Adicione um [SetProperty ControlEvent](setproperty-controlevent.md) à tabela [ControlEvent](controlevent-table.md) que inicializa WaitMessage como FirstMessage sempre que **uma** caixa de diálogo Nova Seleção é aberta. Insira o identificador da caixa de diálogo que vem logo antes da caixa de diálogo Seleção na sequência da caixa de diálogo na coluna \_ Diálogo. Insira o identificador do controle nessa caixa de diálogo usada para abrir a caixa de diálogo Seleção na coluna \_ Controle. Insira \[ WaitMessage \] na coluna Evento. Insira \[ FirstMessage \] na coluna Argument. Insira 1 na coluna Condição e deixe a coluna Ordenação em branco.
12. Adicione [um SetProperty ControlEvent](setproperty-controlevent.md) à tabela [ControlEvent](controlevent-table.md) que define Waitmessage como SecondMessage se o usuário fechar a caixa de diálogo **WaitForCosting** antes que o custo do espaço em disco seja concluído. Insira o identificador da caixa **de diálogo WaitForCosting** na coluna \_ Diálogo. Insira o identificador do controle Texto na coluna \_ Controle. Insira \[ WaitMessage \] na coluna Evento. Insira \[ SecondMessage \] na coluna Argument. Insira NOT [**CostingComplete**](costingcomplete.md) na coluna Condição e deixe a coluna Ordenação em branco.
13. A etapa a seguir vincula o atributo Controle de texto ao ControlEvent que gera a **caixa de diálogo WaitForCosting.** Isso faz com que o instalador passe o valor da propriedade WaitMessage para o atributo controle Text sempre que o usuário abrir uma caixa de **diálogo WaitForCosting.**
14. Assine o atributo Controle de texto do controle Texto para [o SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) que abre a caixa de **diálogo WaitForCosting** adicionando um registro à [tabela EventMapping](eventmapping-table.md). Insira o identificador da caixa **de diálogo WaitForCosting** na coluna \_ Diálogo. Insira o identificador do controle Texto na coluna \_ Controle. Insira SpawnWaitDialog na coluna Evento. Insira Texto, o identificador do atributo Controle de texto, na coluna Atributo da tabela EventMapping.

 

 



