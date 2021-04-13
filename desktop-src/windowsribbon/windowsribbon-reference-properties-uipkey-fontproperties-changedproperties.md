---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifica a \_ Propriedade PKEY \_ fontproperties alterproperties da interface do usuário \_ .
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366466"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>Interface do usuário \_ PKEY \_ fontproperties \_ alteradoproperties

Identifica a \_ Propriedade PKEY \_ fontproperties alterproperties da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ fontproperties \_ alterproperties é usada por um aplicativo para consultar apenas as propriedades alteradas da [interface do usuário \_ PKEY \_ fontproperties](windowsribbon-reference-properties-uipkey-fontproperties.md).

Chamar o método [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) neste objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) retorna um [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).

A interface do usuário \_ PKEY \_ fontproperties \_ alterproperties é passada como o último parâmetro da chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para o aplicativo host da faixa de Ribbon.

Esta chave de propriedade é somente leitura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 