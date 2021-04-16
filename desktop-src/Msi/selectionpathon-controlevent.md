---
description: O controle SelectionTree usa o evento SelectionPathOn para publicar um valor booliano que indica se há um caminho de seleção associado ao recurso selecionado no momento. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757506"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent,

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionPathOn para publicar um valor booliano que indica se há um caminho de seleção associado ao recurso selecionado no momento. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

O SelectionPathOn ControlEvent, nunca é publicado durante uma [instalação de manutenção](maintenance-installation.md).

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree deve assinar o evento por meio da [tabela EventMappings](eventmapping-table.md). O controle de texto exibe a legenda do caminho de seleção. Esse controle de texto é visível ou oculto, dependendo do evento.

 

 



