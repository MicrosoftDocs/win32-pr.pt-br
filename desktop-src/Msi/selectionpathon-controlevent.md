---
description: O controle SelectionTree usa o evento SelectionPathOn para publicar um valor booliana que indica se há um caminho de seleção associado ao recurso selecionado no momento. Esse evento deve ser autor na tabela EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea32926117c200f466bd2c40ac611e7ccbc47fb6a231a5dcf93ffa2ee0446b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040426"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionPathOn para publicar um valor booliana que indica se há um caminho de seleção associado ao recurso selecionado no momento. Esse evento deve ser autor na [tabela EventMapping](eventmapping-table.md).

Esse evento só pode afetar controles localizados na mesma caixa de diálogo que o controle SelectionTree.

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

O SelectionPathOn ControlEvent nunca é publicado durante uma instalação [de manutenção.](maintenance-installation.md)

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um [controle](text-control.md) Texto na mesma caixa de diálogo modal que SelectionTree deve assinar o evento por meio da [tabela EventMapping](eventmapping-table.md). O Controle de Texto exibe a legenda do caminho de seleção. Esse controle de texto é visível ou oculto, dependendo do evento.

 

 



