---
title: UI_PKEY_FontProperties_Bold
description: Identifica a propriedade \_ FontProperties Bold da PKEY \_ da interface do \_ usuário.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444377"
---
# <a name="ui_pkey_fontproperties_bold"></a>\_ \_ FontProperties PKEY da interface do usuário em \_ negrito

Identifica a propriedade \_ FontProperties Bold da PKEY \_ da interface do \_ usuário.

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentários

FontProperties Bold da interface do usuário PKEY é usada por um aplicativo \_ para consultar o estado do botão \_ \_ **Negrito.**

O valor da propriedade é da [**enumeração \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) da interface do usuário.

O valor padrão é `UI_FONTPROPERTIES_NOTSET`.

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|      Propriedade                    |    Resultado da interface do usuário                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **O** botão negrito está desabilitado e só pode ser definido pelo aplicativo. |
| `UI_FONTPROPERTIES_NOTSET`       | **O** botão Negrito não está selecionado.                                    |
| `UI_FONTPROPERTIES_SET`          | **O botão** Negrito está selecionado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTPROPERTIES da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 