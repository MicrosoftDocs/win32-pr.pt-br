---
description: O controle SelectionTree usa esse evento para publicar uma cadeia de caracteres que descreve o item realçado. A cadeia de caracteres é uma das &\# 0034; Sel \* & \# 0034; cadeias de caracteres da tabela UIText. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: ControlEvent, selectionaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769307"
---
# <a name="selectionaction-controlevent"></a>ControlEvent, selectionaction

O [controle SelectionTree](selectiontree-control.md) usa esse evento para publicar uma cadeia de caracteres que descreve o item realçado. A cadeia de caracteres é uma das \* cadeias "SEL" da [tabela UIText](uitext-table.md). Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree deve assinar esse evento por meio da [tabela EventMappings](eventmapping-table.md). O controle de texto exibe a explicação do item selecionado.

 

 



