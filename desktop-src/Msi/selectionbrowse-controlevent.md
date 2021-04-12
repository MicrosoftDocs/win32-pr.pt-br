---
description: O controle SelectionTree usa o evento SelectionBrowse para gerar uma caixa de diálogo de procura, tornando possível modificar o caminho do item realçado.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297694"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent,

O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionBrowse para gerar uma caixa de diálogo de **procura** , tornando possível modificar o caminho do item realçado.

Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento. O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Todos os controles que publicarem um evento SelectionBrowse serão desabilitados se um recurso tiver sido selecionado e já estiver instalado, não configurável ou não estiver selecionado para instalação local. Para ser configurável, o recurso deve ter uma [propriedade pública](public-properties.md) inserida no \_ campo diretório da [tabela de recursos](feature-table.md).

## <a name="published-by"></a>Publicada por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

O nome da caixa de diálogo a ser gerada.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Nenhum.

## <a name="typical-use"></a>Usos comum

Um controle de [pressão](pushbutton-control.md) na mesma caixa de diálogo modal que o SelectionTree usa esse evento para disparar a caixa de diálogo **procurar** .

 

 



