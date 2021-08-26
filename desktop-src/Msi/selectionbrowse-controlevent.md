---
description: O controle SelectionTree usa o evento SelectionBrowse para gerar uma caixa de diálogo Procurar, possibilitando modificar o caminho do item realçado.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70d7c50e69921a5fefe7cff3c88c2351cacdecda42a164e8334c9afb3977bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040606"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionBrowse para gerar uma caixa de diálogo Procurar, possibilitando **modificar** o caminho do item realçado.

Esse evento deve ser publicado por um [Controle PushButton](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle que assina esse evento. O evento deve ser autor na [tabela ControlEvent](controlevent-table.md).

Esse ControlEvent exige que a interface do usuário seja executado no [*nível completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida ou*](r-gly.md) interface do usuário [*básica.*](b-gly.md) Para obter informações, consulte [Interface do Usuário níveis .](user-interface-levels.md)

Todos os controles que publicam um evento SelectionBrowse serão desabilitados se um recurso já estiver instalado, não configurável ou não selecionado para instalação local. Para ser configurável, o recurso deve ter uma [propriedade pública](public-properties.md) inserida no campo Diretório da \_ tabela [Recurso](feature-table.md).

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

O nome da caixa de diálogo a ser gerada.

## <a name="action-on-subscribers"></a>Ação em Assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um [controle PushButton](pushbutton-control.md) na mesma caixa de diálogo modal que SelectionTree usa esse evento para disparar a **caixa de** diálogo Procurar.

 

 



