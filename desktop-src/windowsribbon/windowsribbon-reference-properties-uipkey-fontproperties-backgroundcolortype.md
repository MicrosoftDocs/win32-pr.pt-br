---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica a propriedade backgroundcolortype da interface do usuário \_ PKEY \_ FontProperty \_ .
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454102"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="97984-103">IU \_ PKEY \_ FontProperty \_ backgroundcolortype</span><span class="sxs-lookup"><span data-stu-id="97984-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="97984-104">Identifica a propriedade backgroundcolortype da interface do usuário \_ PKEY \_ FontProperty \_ .</span><span class="sxs-lookup"><span data-stu-id="97984-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="97984-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="97984-105">Remarks</span></span>

<span data-ttu-id="97984-106">A interface do usuário \_ PKEY \_ FontProperty \_ backgroundcolortype é usada por um aplicativo, em conjunto com a [interface do usuário \_ PKEY \_ fontproperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), para consultar as configurações da Galeria de **cores de realce de texto** .</span><span class="sxs-lookup"><span data-stu-id="97984-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="97984-107">O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="97984-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="97984-108">O valor padrão é `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="97984-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="97984-109">A tabela a seguir descreve os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="97984-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="97984-110">O aplicativo deve consultar a métrica do sistema apropriada para o valor de cor normalmente a **cor de fundo da janela** de tema atual do Windows que é recuperada com GetSysColor (janela de cores \_ ).</span><span class="sxs-lookup"><span data-stu-id="97984-110">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="97984-111">Não há suporte para o [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="97984-111">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="97984-112">O aplicativo deve consultar a [interface do usuário \_ PKEY \_ fontproperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) para o valor de cor.</span><span class="sxs-lookup"><span data-stu-id="97984-112">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="97984-113">O valor de cor da [interface do usuário \_ PKEY \_ fontproperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) é exibido no botão de **cor de realce de texto** e selecionado na Galeria de cores de **realce de texto** .</span><span class="sxs-lookup"><span data-stu-id="97984-113">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="97984-114">A interface do usuário \_ PKEY \_ FontProperty \_ backgroundcolortype é passada para o método de retorno de chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em uma galeria de **cores de realce de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="97984-114">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="97984-115">É altamente recomendável que o aplicativo defina apenas um valor de **cor de realce de texto** inicial e não redefina esse valor quando o cursor for reposicionado em um documento.</span><span class="sxs-lookup"><span data-stu-id="97984-115">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="97984-116">A última seleção deve ser mantida para evitar a necessidade de selecionar novamente a cor desejada.</span><span class="sxs-lookup"><span data-stu-id="97984-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="97984-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97984-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97984-118">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="97984-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="97984-119">**SWATCHCOLORTYPE da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="97984-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="97984-120">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="97984-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

