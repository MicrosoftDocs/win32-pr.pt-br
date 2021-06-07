---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica a propriedade \_ \_ FontProperties BackgroundColorType da interface do \_ usuário PKEY.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443817"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="7bf62-103">\_ \_ FontProperties \_ BackgroundColorType da interface do usuário PKEY</span><span class="sxs-lookup"><span data-stu-id="7bf62-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="7bf62-104">Identifica a propriedade \_ \_ FontProperties BackgroundColorType da interface do \_ usuário PKEY.</span><span class="sxs-lookup"><span data-stu-id="7bf62-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="7bf62-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bf62-105">Remarks</span></span>

<span data-ttu-id="7bf62-106">UI PKEY FontProperties BackgroundColorType é usado por um aplicativo, em conjunto com a interface do usuário \_ \_ \_ [ \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor),  para consultar as configurações da galeria de cores de realçadas de texto.</span><span class="sxs-lookup"><span data-stu-id="7bf62-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="7bf62-107">O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7bf62-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="7bf62-108">O valor padrão é `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="7bf62-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="7bf62-109">A tabela a seguir descreve os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7bf62-109">The following table describes the property values.</span></span>



|   <span data-ttu-id="7bf62-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7bf62-110">Property</span></span>                             |   <span data-ttu-id="7bf62-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7bf62-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="7bf62-112">O aplicativo deve consultar a métrica do sistema apropriada  para o valor de cor normalmente a cor da tela de fundo da janela de tema atual do Windows que é recuperada com GetSysColor(COLOR \_ WINDOW).</span><span class="sxs-lookup"><span data-stu-id="7bf62-112">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="7bf62-113">Sem suporte do [**FontControl.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="7bf62-113">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="7bf62-114">O aplicativo deve consultar [ \_ \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) da interface do usuário para o valor de cor.</span><span class="sxs-lookup"><span data-stu-id="7bf62-114">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="7bf62-115">O valor de cor da interface do usuário [ \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) é exibido no botão Cor de realçada de texto e selecionado na Galeria de cores de **realçada de** texto. </span><span class="sxs-lookup"><span data-stu-id="7bf62-115">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="7bf62-116">FontProperties BackgroundColorType da interface do usuário PKEY é passado para o método de retorno de chamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  quando um swatch de cor é selecionado em uma galeria de cores de realçamento de Texto [**FontControl.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="7bf62-116">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="7bf62-117">É altamente recomendável que o  aplicativo desem conjunto apenas um valor de cor de realçaamento de texto inicial e não de novo esse valor quando o cursor é reposicionado dentro de um documento.</span><span class="sxs-lookup"><span data-stu-id="7bf62-117">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="7bf62-118">A última seleção deve ser mantida para evitar a necessidade de selecionar a cor desejada.</span><span class="sxs-lookup"><span data-stu-id="7bf62-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7bf62-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bf62-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bf62-120">Propriedades do controle de fonte</span><span class="sxs-lookup"><span data-stu-id="7bf62-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="7bf62-121">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="7bf62-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="7bf62-122">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="7bf62-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

