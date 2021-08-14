---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifica a propriedade \_ \_ QuickAccessToolbarDock da PKEY da interface do usuário.
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9011cceb9b2ec96680ea3badd0ad40ae6121c14a70e065cfbfff5f5fe8e1f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201366"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>\_QuickAccessToolbarDock da interface do usuário \_

Identifica a propriedade \_ \_ QuickAccessToolbarDock da PKEY da interface do usuário.

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

O \_ QuickAccessToolbarDock da interface do usuário do PKEY é usado por um aplicativo para consultar o estado de encaixe da QAT (Barra de Ferramentas de Acesso \_ Rápido).

O valor da propriedade é da [**enumeração \_ CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) da interface do usuário.



|    Enumeração                     |    Descrição                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTROLE DE INTERFACE \_ DO USUÁRIODOCK \_ TOP    | O QAT é encaixado na área não dependente do aplicativo host da Faixa de Opções, conforme mostrado na captura de tela a seguir.![captura de tela da barra de ferramentas de acesso rápido encaixada acima da faixa de opções na área não dependente.](images/properties/qat-docktop.png)<br/> |
| CONTROLE DE INTERFACE \_ DO USUÁRIOBAIXO \_ INFERIOR | O QAT é encaixado como uma faixa visualmente integral abaixo da Faixa de Opções, conforme mostrado na captura de tela a seguir. ![captura de tela da barra de ferramentas de acesso rápido encaixada abaixo da faixa de opções.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da faixa de opções](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

