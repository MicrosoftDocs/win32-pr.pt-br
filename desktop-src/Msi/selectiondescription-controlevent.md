---
description: O controle SelectionTree usa o evento SelectionDescription para publicar uma cadeia de caracteres que contém a descrição do item realçado. Essa cadeia de caracteres é o campo de descrição da tabela de recursos. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753435"
---
# <a name="selectiondescription-controlevent"></a>SelectionDescription ControlEvent,

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionDescription para publicar uma cadeia de caracteres que contém a descrição do item realçado. Essa cadeia de caracteres é o campo de **Descrição** da [tabela de recursos](feature-table.md). Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o [controle SelectionTree](selectiontree-control.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree assina esse ControlEvent, por meio da [tabela EventMappings](eventmapping-table.md). O controle de texto usa esse evento para exibir a descrição do item realçado.

 

 



