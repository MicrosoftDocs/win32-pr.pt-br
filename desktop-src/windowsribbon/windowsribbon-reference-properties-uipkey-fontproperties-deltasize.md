---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007564"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="383c4-103">Interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize</span><span class="sxs-lookup"><span data-stu-id="383c4-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="383c4-104">Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize.</span><span class="sxs-lookup"><span data-stu-id="383c4-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="383c4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="383c4-105">Remarks</span></span>

<span data-ttu-id="383c4-106">A interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize é usada por um aplicativo em casos em que não é possível que o aplicativo especifique um valor para o **tamanho da fonte**, como quando uma execução de texto de tamanho heterogêneo é selecionada.</span><span class="sxs-lookup"><span data-stu-id="383c4-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="383c4-107">O controle **tamanho da fonte** está definido como em branco e a interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize é usada para capturar a interação do usuário com os botões **aumentar fonte** e **reduzir fonte** .</span><span class="sxs-lookup"><span data-stu-id="383c4-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="383c4-108">A interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize está incluída na [interface do usuário \_ PKEY \_ fontproperties \_ alterproperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="383c4-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="383c4-109">A captura de tela a seguir mostra os botões **aumentar fonte** e **redução de fonte** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="383c4-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de tela dos botões aumentar fonte e reduzir fonte no fontcontrol.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="383c4-111">A tabela a seguir descreve os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="383c4-111">The following table describes the property values.</span></span>



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="383c4-112">Botão **aumentar fonte** clicado.</span><span class="sxs-lookup"><span data-stu-id="383c4-112">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="383c4-113">Botão **reduzir fonte** clicado.</span><span class="sxs-lookup"><span data-stu-id="383c4-113">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="383c4-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="383c4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="383c4-115">Propriedades de controle de fonte</span><span class="sxs-lookup"><span data-stu-id="383c4-115">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="383c4-116">**FONTDELTASIZE da interface do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="383c4-116">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="383c4-117">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="383c4-117">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 