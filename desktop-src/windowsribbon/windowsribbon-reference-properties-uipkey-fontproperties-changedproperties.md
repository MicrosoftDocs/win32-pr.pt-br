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
# <a name="ui_pkey_fontproperties_changedproperties"></a><span data-ttu-id="d21af-103">Interface do usuário \_ PKEY \_ fontproperties \_ alteradoproperties</span><span class="sxs-lookup"><span data-stu-id="d21af-103">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>

<span data-ttu-id="d21af-104">Identifica a \_ Propriedade PKEY \_ fontproperties alterproperties da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="d21af-104">Identifies the UI\_PKEY\_FontProperties\_ChangedProperties property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a><span data-ttu-id="d21af-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d21af-105">Remarks</span></span>

<span data-ttu-id="d21af-106">A interface do usuário \_ PKEY \_ fontproperties \_ alterproperties é usada por um aplicativo para consultar apenas as propriedades alteradas da [interface do usuário \_ PKEY \_ fontproperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span><span class="sxs-lookup"><span data-stu-id="d21af-106">UI\_PKEY\_FontProperties\_ChangedProperties is used by an application to query only changed properties from [UI\_PKEY\_FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span></span>

<span data-ttu-id="d21af-107">Chamar o método [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) neste objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) retorna um [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d21af-107">Calling the [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method on this [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object returns an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

<span data-ttu-id="d21af-108">A interface do usuário \_ PKEY \_ fontproperties \_ alterproperties é passada como o último parâmetro da chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para o aplicativo host da faixa de Ribbon.</span><span class="sxs-lookup"><span data-stu-id="d21af-108">UI\_PKEY\_FontProperties\_ChangedProperties is passed as the last parameter of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) call to the Ribbon host application.</span></span>

<span data-ttu-id="d21af-109">Esta chave de propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d21af-109">This property key is read-only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d21af-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d21af-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d21af-111">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="d21af-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d21af-112">**IUISimplePropertySet**</span><span class="sxs-lookup"><span data-stu-id="d21af-112">**IUISimplePropertySet**</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[<span data-ttu-id="d21af-113">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="d21af-113">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 