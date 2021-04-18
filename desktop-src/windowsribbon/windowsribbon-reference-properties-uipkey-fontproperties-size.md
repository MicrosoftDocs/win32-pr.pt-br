---
title: UI_PKEY_FontProperties_Size
description: Identifica a propriedade de tamanho da interface do usuário \_ PKEY \_ fontproperties \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761914"
---
# <a name="ui_pkey_fontproperties_size"></a><span data-ttu-id="8acc8-103">\_Tamanho da \_ fonte de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="8acc8-103">UI\_PKEY\_FontProperties\_Size</span></span>

<span data-ttu-id="8acc8-104">Identifica a propriedade de tamanho da interface do usuário \_ PKEY \_ fontproperties \_ .</span><span class="sxs-lookup"><span data-stu-id="8acc8-104">Identifies the UI\_PKEY\_FontProperties\_Size property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a><span data-ttu-id="8acc8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8acc8-105">Remarks</span></span>

<span data-ttu-id="8acc8-106">\_O tamanho da fonte de PKEY da interface do usuário \_ \_ é usado por um aplicativo para consultar o valor do controle de **tamanho da fonte** .</span><span class="sxs-lookup"><span data-stu-id="8acc8-106">UI\_PKEY\_FontProperties\_Size is used by an application to query the value of the **Font size** control.</span></span>

<span data-ttu-id="8acc8-107">Os valores válidos para esse intervalo de propriedade são de 1 a 9999, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8acc8-107">Valid values for this property range from 1 to 9999, inclusive.</span></span> <span data-ttu-id="8acc8-108">Se um usuário tentar inserir um valor inválido, a entrada será rejeitada e o controle de **tamanho da fonte** reverterá para o último valor válido.</span><span class="sxs-lookup"><span data-stu-id="8acc8-108">If a user tries to enter an invalid value, the entry is rejected and the **Font size** control reverts to the last valid value.</span></span>

<span data-ttu-id="8acc8-109">Se um aplicativo tentar definir o tamanho da fonte programaticamente para um valor fora do intervalo válido, a estrutura da faixa de opções invalidará todas as propriedades de fonte e definirá os controles de fonte (**tamanho da fonte** e **face da fonte**) como em branco ou com seu estado padrão, quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="8acc8-109">If an application attempts to set font size programmatically to a value outside the valid range, the Ribbon framework invalidates all font properties and sets the font controls (**Font size** and **Font face**) to blank or to their default state, where appropriate.</span></span>

<span data-ttu-id="8acc8-110">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="8acc8-110">The default value is 0.</span></span>

<span data-ttu-id="8acc8-111">Um valor de 0 especifica que nenhum único tamanho de ponto é selecionado (nenhum texto ou uma execução de texto de tamanho heterogêneo, é selecionado).</span><span class="sxs-lookup"><span data-stu-id="8acc8-111">A value of 0 specifies that no single point size is selected (either no text, or a run of heterogeneously sized text, is selected).</span></span>

<span data-ttu-id="8acc8-112">Um usuário não pode definir o controle de **tamanho da fonte** como 0.</span><span class="sxs-lookup"><span data-stu-id="8acc8-112">A user cannot set the **Font size** control to 0.</span></span>

<span data-ttu-id="8acc8-113">Diferente de 0, os valores válidos para a interface do usuário \_ PKEY \_ fontproperties \_ dimensionar intervalo entre *MinimumFontSize* e *MaximumFontSize* como declarado na marcação de [controle de fonte](windowsribbon-controls-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="8acc8-113">Other than 0, valid values for UI\_PKEY\_FontProperties\_Size range between *MinimumFontSize* and *MaximumFontSize* as declared in the [Font Control](windowsribbon-controls-fontcontrol.md) markup.</span></span>

> [!Note]  
> <span data-ttu-id="8acc8-114">O controle **tamanho da fonte** é definido como em branco quando o tamanho da fonte é definido por meio de programação como 0, como quando uma execução de texto de tamanho heterogêneo é realçada.</span><span class="sxs-lookup"><span data-stu-id="8acc8-114">The **Font size** control is set to blank when the font size is programmatically set to 0, such as when a run of heterogeneously sized text is highlighted.</span></span>

 

<span data-ttu-id="8acc8-115">Quando uma execução de texto de tamanho heterogêneo é selecionada, o aplicativo deve consultar a [interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) para capturar **aumentar a fonte** e reduzir os comandos de **fonte** .</span><span class="sxs-lookup"><span data-stu-id="8acc8-115">Where a run of heterogeneously sized text is selected, the application should query [UI\_PKEY\_FontProperties\_DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) to capture **Grow font** and **Shrink font** commands.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8acc8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8acc8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8acc8-117">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="8acc8-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="8acc8-118">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="8acc8-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




