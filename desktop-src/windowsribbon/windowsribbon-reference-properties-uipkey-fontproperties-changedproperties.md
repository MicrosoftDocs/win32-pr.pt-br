---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifica a propriedade \_ \_ FontProperties \_ ChangedProperties da IU PKEY.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36262a9acf217e448956f108b68cb0716b5b5080c71f6a2a8e305c9e59478c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028654"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>Fonte \_ PKEY da \_ interface do usuárioPropriedades \_ AlteradasPropriedades

Identifica a propriedade \_ \_ FontProperties \_ ChangedProperties da IU PKEY.

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

FontProperties ChangedProperties da interface do usuário PKEY é usada por um aplicativo para consultar somente as propriedades alteradas da interface do usuário \_ \_ \_ [ \_ PKEY \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).

Chamar [**o método IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) neste objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) retorna [um IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).

A interface do usuário PKEY FontProperties ChangedProperties é passada como o último parâmetro da chamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para o aplicativo host da Faixa de Opções.

Essa chave de propriedade é somente leitura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 