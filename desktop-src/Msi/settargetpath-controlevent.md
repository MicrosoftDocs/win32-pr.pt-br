---
description: O evento SetTargetPath notifica o instalador para verificar e definir o caminho selecionado. Se o caminho não for válido para gravação, o instalador bloqueará ControlEvents adicionais associados ao controle.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e49e9447d7d2e67dce85e7d60638c18a949ecbc87800d12a60bc94d971cb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625066"
---
# <a name="settargetpath-controlevent"></a>SetTargetPath ControlEvent,

O evento SetTargetPath notifica o instalador para verificar e definir o caminho selecionado. Se o caminho não for válido para gravação, o instalador bloqueará ControlEvents adicionais associados ao controle.

Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md). Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

O nome da propriedade que contém o caminho. Se a propriedade for indireta, o nome da propriedade será colocado entre colchetes.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo de procura está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para verificar o caminho selecionado antes de retornar à caixa de diálogo de seleção.

## <a name="remarks"></a>Comentários

Não tente configurar o caminho de destino se os componentes que usam esses caminhos já estiverem instalados para o usuário atual ou para um usuário diferente. Verifique a propriedade [**productstate**](productstate.md) antes de publicar o SetTargetPath ControlEvent, para determinar se o produto que contém o componente está instalado.

 

 



