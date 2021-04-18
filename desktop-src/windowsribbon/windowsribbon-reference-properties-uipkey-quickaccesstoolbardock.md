---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica a \_ Propriedade PKEY QuickAccessToolbarDock da interface do usuário \_ .
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366096"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>\_QuickAccessToolbarDock PKEY \_ UI

Identifica a \_ Propriedade PKEY QuickAccessToolbarDock da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ QuickAccessToolbarDock é usada por um aplicativo para consultar o estado de encaixe da barra de ferramentas de acesso rápido (qat).

O valor da propriedade é da [**enumeração \_ CONTROLDOCK da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ parte superior da interface do usuário CONTROLDOCK    | O QAT é encaixado na área não cliente do aplicativo host da faixa de opções, conforme mostrado na captura de tela a seguir.![captura de tela da barra de ferramentas de acesso rápido encaixada acima da faixa de opções na área não cliente.](images/properties/qat-docktop.png)<br/> |
| \_CONTROLDOCK \_ inferior da interface do usuário | O QAT é encaixado como uma faixa visualmente integral abaixo da faixa de opções, conforme mostrado na captura de tela a seguir. ![captura de tela da barra de ferramentas de acesso rápido encaixada abaixo da faixa de faixas.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da faixa de faixas](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

