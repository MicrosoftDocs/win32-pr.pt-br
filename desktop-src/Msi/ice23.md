---
description: ICE23 valida a ordem de tabulação de controle para cada caixa de diálogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbab2d50c07fce208edc845e64cff0061f513c102a55da2d56b49c4a4c17e867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528996"
---
# <a name="ice23"></a>ICE23

ICE23 valida a ordem de tabulação de controle para cada caixa de diálogo.

ICE23 valida o seguinte na tabela de [diálogo](dialog-table.md) e na [tabela de controle](control-table.md):

-   Cada registro na tabela de diálogo especifica um controle na \_ primeira coluna de controle que existe na caixa de diálogo especificada pela coluna de caixa de diálogo.
-   Cada registro na tabela de controle Especifica um controle na \_ próxima coluna de controle que está na mesma caixa de diálogo que o controle listado na coluna de controle, ou \_ o controle a seguir contém o valor nulo.
-   Que seguir o controle \_ próximo entradas do controle para o controle na tabela de controle faz um loop único, fechado, que retorna ao controle inicial. Nem todo controle precisa estar no loop, mas o loop deve passar por cada controle que tenha uma entrada na próxima coluna de controle \_ .

## <a name="result"></a>Resultado

ICE23 posta uma mensagem de erro se a ordem de tabulação dos controles não formar um loop fechado único na caixa de diálogo.

## <a name="example"></a>Exemplo

ICE23 postaria as seguintes mensagens de erro para o exemplo mostrado.

-   Dialog1 não tem controle \_ primeiro.
-   O controle \_ primeiro da caixa de diálogo Dialog2 refere-se a um ControlX de controle inexistente.
-   Dialog3 tem uma ordem de tabulação de inatividade no controle ControlB.
-   Dialog4 tem ordem de tabulação malformada no controle ControlC
-   Dialog5 tem uma ordem de tabulação malformada no controle ControlC.
-   Controle o \_ próximo do controle Dialog6. ControlC vincula-se a um controle desconhecido.

[Tabela de diálogo](dialog-table.md) (parcial)



| caixa de diálogo  | Controlar \_ primeiro |
|---------|----------------|
| Dialog1 |                |
| Dialog2 | ControlX       |
| Dialog3 | ControlA       |
| Dialog4 | ControlA       |
| Dialog5 | ControlA       |



 

[Tabela de controle](control-table.md) (parcial)



| caixa de diálogo  | Control  | \_Próximo controle |
|---------|----------|---------------|
| Dialog1 | ControlA |               |
| Dialog1 | ControlB | ControlA      |
| Dialog2 | ControlA | ControlB      |
| Dialog2 | ControlB | ControlA      |
| Dialog3 | ControlA | ControlB      |
| Dialog3 | ControlB |               |
| Dialog4 | ControlA | ControlB      |
| Dialog4 | ControlB | ControlC      |
| Dialog4 | ControlC | ControlB      |
| Dialog5 | ControlA | ControlB      |
| Dialog5 | ControlB | ControlC      |
| Dialog5 | ControlC | ControlA      |
| Dialog5 | Controle | ControlA      |
| Dialog6 | ControlA | ControlB      |
| Dialog6 | ControlB | ControlC      |
| Dialog6 | ControlC | ControlX      |
| Dialog6 | Controle | ControlA      |



 

Para corrigir esses erros, observe o seguinte nas tabelas acima e faça as alterações indicadas.

Nem todas as linhas na tabela de diálogo têm um controle especificado na \_ primeira coluna do controle. Altere a \_ primeira coluna Control do registro Dialog1 na tabela Dialog para um controle que exista em Dialog1.

Nem toda linha na tabela de diálogo tem um controle especificado na \_ primeira coluna de controle que existe na caixa de diálogo. Altere a \_ primeira coluna do controle Dialog2 para um controle que exista em Dialog2.

Seguindo o controle \_ próximo entradas na tabela de controle do controle para o controle não faz um loop fechado em todos os casos. Altere a \_ próxima coluna do controle para ControlB em Dialog3 para controla.

Após o controle, \_ as próximas entradas na tabela de controle do controle ao controle não retornam ao controle inicial em todos os casos. Altere a \_ próxima coluna do controle para ControlC em Dialog4 para fazer referência a controla.

Após o controle, \_ as próximas entradas na tabela de controle do controle ao controle não passam por todos os controles na caixa de diálogo com uma entrada na \_ próxima coluna do controle. Altere a \_ próxima coluna do controle para ControlC em Dialog5 para controle.

\_O controle Next não se refere a um controle válido que está na mesma caixa de diálogo que o controle listado na coluna Control. Altere a \_ próxima coluna do controle para ControlC em Dialog6 para referir-se ao controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



