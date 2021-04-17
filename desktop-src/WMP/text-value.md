---
title: TEXT. Value
description: O atributo Value especifica ou recupera o texto que é exibido no controle de texto.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- TEXT. Value Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747894"
---
# <a name="textvalue"></a><span data-ttu-id="68b0b-104">TEXT. Value</span><span class="sxs-lookup"><span data-stu-id="68b0b-104">TEXT.value</span></span>

<span data-ttu-id="68b0b-105">O atributo **Value** especifica ou recupera o texto que é exibido no controle de texto.</span><span class="sxs-lookup"><span data-stu-id="68b0b-105">The **value** attribute specifies or retrieves the text that is displayed in the Text control.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="68b0b-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="68b0b-106">Possible Values</span></span>

<span data-ttu-id="68b0b-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="68b0b-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b0b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="68b0b-108">Remarks</span></span>

<span data-ttu-id="68b0b-109">Se a largura do controle de texto não for suficiente para conter o texto fornecido, o texto será cortado e uma elipse será mostrada para ilustrar o fato.</span><span class="sxs-lookup"><span data-stu-id="68b0b-109">If the width of the Text control is insufficient to contain the text provided, the text is cropped, and an ellipsis is shown to illustrate the fact.</span></span> <span data-ttu-id="68b0b-110">Se o atributo **ToolTip** não tiver sido definido, o texto completo será exibido como uma dica de ferramenta quando o cursor passar sobre o controle.</span><span class="sxs-lookup"><span data-stu-id="68b0b-110">If the **toolTip** attribute has not been set, the complete text will then appear as a ToolTip when the cursor hovers over the control.</span></span>

<span data-ttu-id="68b0b-111">Se uma largura não for especificada, a largura padrão do controle será a largura da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="68b0b-111">If a width is not specified, the default width for the control is the width of the string.</span></span>

<span data-ttu-id="68b0b-112">Se a altura do controle não for especificada, a altura padrão será uma linha.</span><span class="sxs-lookup"><span data-stu-id="68b0b-112">If the height of the control is not specified, the default height is one line.</span></span>

<span data-ttu-id="68b0b-113">Se o atributo **WordWrap** for definido como true e a altura do controle for suficiente para acomodar outra linha de texto, o texto será quebrado em uma linha subsequente.</span><span class="sxs-lookup"><span data-stu-id="68b0b-113">If the **wordWrap** attribute is set to true and the height of the control is enough to accommodate another line of text, the text wraps to a subsequent line.</span></span> <span data-ttu-id="68b0b-114">O encapsulamento ocorre apenas entre palavras.</span><span class="sxs-lookup"><span data-stu-id="68b0b-114">Wrapping only occurs between words.</span></span> <span data-ttu-id="68b0b-115">Quebras de linha também podem ser forçadas, conforme explicado em **WordWrap**.</span><span class="sxs-lookup"><span data-stu-id="68b0b-115">Line breaks may also be forced, as explained under **wordWrap**.</span></span>

## <a name="examples"></a><span data-ttu-id="68b0b-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="68b0b-116">Examples</span></span>

<span data-ttu-id="68b0b-117">O exemplo a seguir é um arquivo de definição de capa completo que ilustra como os atributos do elemento de **texto** são usados.</span><span class="sxs-lookup"><span data-stu-id="68b0b-117">The following sample is a complete skin definition file that illustrates how the attributes of the **TEXT** element are used.</span></span> <span data-ttu-id="68b0b-118">Ele pode ser encontrado no diretório de exemplos que foi instalado com o SDK.</span><span class="sxs-lookup"><span data-stu-id="68b0b-118">It can be found in the Samples directory that was installed with the SDK.</span></span>


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="68b0b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b0b-119">Requirements</span></span>



| <span data-ttu-id="68b0b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b0b-120">Requirement</span></span> | <span data-ttu-id="68b0b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="68b0b-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="68b0b-122">Versão</span><span class="sxs-lookup"><span data-stu-id="68b0b-122">Version</span></span><br/> | <span data-ttu-id="68b0b-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="68b0b-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68b0b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="68b0b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b0b-125">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="68b0b-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="68b0b-126">**TEXT. toolTip**</span><span class="sxs-lookup"><span data-stu-id="68b0b-126">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="68b0b-127">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="68b0b-127">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





