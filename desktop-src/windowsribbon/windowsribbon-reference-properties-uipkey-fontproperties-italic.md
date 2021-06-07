---
title: UI_PKEY_FontProperties_Italic
description: Identifica a propriedade \_ IU PKEY \_ FontProperties \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443807"
---
# <a name="ui_pkey_fontproperties_italic"></a>Fonte \_ de PKEY \_ da interface do usuárioPropriedades \_ itálico

Identifica a propriedade \_ IU PKEY \_ FontProperties \_ Italic.

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentários

A \_ interface do usuário \_ PKEY FontProperties Italic é usada por um aplicativo para consultar o \_ estado do botão **Itálico.**

O valor da propriedade é da [**enumeração \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) da interface do usuário.

O valor padrão é `UI_FONTPROPERTIES_NOTSET`.

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|    Propriedade                      |       Resultado da interface do usuário                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | **O botão Itálico** está desabilitado e só pode ser definido pelo aplicativo. |
| `UI_FONTPROPERTIES_NOTSET`       | **O botão Itálico** não está selecionado.                                    |
| `UI_FONTPROPERTIES_SET`          | **O botão Itálico** está selecionado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTPROPERTIES da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 