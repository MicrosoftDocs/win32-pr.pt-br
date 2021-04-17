---
description: 'A sintaxe para o evento SetProperty é diferente de para outros ControlEvents no lugar do nome do evento que coloca a propriedade entre colchetes: \[ nome da propriedade \_ \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: ControlEvent, SetProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758616"
---
# <a name="setproperty-controlevent"></a>ControlEvent, SetProperty

A sintaxe para o evento SetProperty é diferente de para outros ControlEvents no lugar do nome do evento que coloca a propriedade entre colchetes: \[ nome da propriedade \_ \] . O argumento é o novo valor da propriedade. Para remover a propriedade, o argumento deve ser {} . Isso é necessário, porque o argumento é uma chave primária na tabela e, portanto, não pode ser nulo. O argumento será formatado usando o método FormatText, portanto, o argumento pode conter qualquer expressão que o método FormatText possa manipular. Os valores de propriedade são avaliados no momento do ControlEvent,.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

O novo valor da propriedade. {} para NULL.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo vinculada a esse evento para que ele altere uma propriedade quando o botão é enviado por push.

 

 



