---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366271"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="10943-103">Interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="10943-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="10943-104">Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType.</span><span class="sxs-lookup"><span data-stu-id="10943-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="10943-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="10943-105">Remarks</span></span>

<span data-ttu-id="10943-106">A interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType é usada por um aplicativo, em conjunto com a [interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), para consultar as configurações da Galeria de **cores de texto** .</span><span class="sxs-lookup"><span data-stu-id="10943-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="10943-107">O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="10943-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="10943-108">O valor padrão é `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="10943-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="10943-109">A tabela a seguir descreve os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="10943-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="10943-110">Não há suporte para o [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="10943-110">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="10943-111">O aplicativo deve consultar a métrica de sistema apropriada para o valor de cor normalmente a **cor de texto** do tema do Windows atual que é recuperada com GETSYSCOLOR (Color \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="10943-111">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="10943-112">O aplicativo deve consultar a [interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) para o valor de cor.</span><span class="sxs-lookup"><span data-stu-id="10943-112">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="10943-113">O valor de cor da [interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) é exibido no botão de **cor do texto** e selecionado na Galeria de cores de **texto** .</span><span class="sxs-lookup"><span data-stu-id="10943-113">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="10943-114">A interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType é passada para o método de retorno de chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em uma galeria de **cores de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="10943-114">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="10943-115">É altamente recomendável que o aplicativo defina apenas um valor de **cor de texto** inicial e não redefina esse valor quando o cursor for reposicionado em um documento.</span><span class="sxs-lookup"><span data-stu-id="10943-115">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="10943-116">A última seleção deve ser mantida para evitar a necessidade de selecionar novamente a cor desejada.</span><span class="sxs-lookup"><span data-stu-id="10943-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="10943-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10943-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10943-118">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="10943-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="10943-119">**SWATCHCOLORTYPE da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="10943-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="10943-120">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="10943-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

