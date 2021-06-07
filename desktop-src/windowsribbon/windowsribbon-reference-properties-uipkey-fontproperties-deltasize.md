---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica a propriedade \_ \_ FontProperties DeltaSize da PKEY da interface do \_ usuário.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444387"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="da9ac-103">Interface \_ do usuário \_ FontProperties \_ DeltaSize</span><span class="sxs-lookup"><span data-stu-id="da9ac-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="da9ac-104">Identifica a propriedade \_ \_ FontProperties DeltaSize da PKEY da interface do \_ usuário.</span><span class="sxs-lookup"><span data-stu-id="da9ac-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="da9ac-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="da9ac-105">Remarks</span></span>

<span data-ttu-id="da9ac-106">A interface do usuário \_ \_ PKEY FontProperties \_ DeltaSize é usada por um aplicativo em casos em que não é possível que o aplicativo especifique um valor para Tamanho da fonte, como quando uma operação de texto de tamanho heterogêneo é selecionada.</span><span class="sxs-lookup"><span data-stu-id="da9ac-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="da9ac-107">O **controle** Tamanho da fonte é definido como em branco e \_ \_ FontProperties \_ DeltaSize   da interface do usuário É usado para capturar a interação do usuário com os botões Aumentar fonte e Reduzir fonte.</span><span class="sxs-lookup"><span data-stu-id="da9ac-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="da9ac-108">UI PKEY FontProperties DeltaSize está incluído na interface do usuário \_ \_ \_ [ \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="da9ac-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="da9ac-109">A captura de tela a seguir mostra os **botões Aumentar e** Reduzir fonte da Faixa de Opções [**FontControl.**](windowsribbon-element-fontcontrol.md) </span><span class="sxs-lookup"><span data-stu-id="da9ac-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![captura de tela dos botões de redução de fonte e de crescimento de fonte no controle de fonte.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="da9ac-111">A tabela a seguir descreve os valores da propriedade.</span><span class="sxs-lookup"><span data-stu-id="da9ac-111">The following table describes the property values.</span></span>



|     <span data-ttu-id="da9ac-112">Valor</span><span class="sxs-lookup"><span data-stu-id="da9ac-112">Value</span></span>                 |  <span data-ttu-id="da9ac-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="da9ac-113">Description</span></span>                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="da9ac-114">**Botão Aumentar fonte** clicado.</span><span class="sxs-lookup"><span data-stu-id="da9ac-114">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="da9ac-115">**Botão Reduzir** fonte clicado.</span><span class="sxs-lookup"><span data-stu-id="da9ac-115">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="da9ac-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da9ac-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da9ac-117">Propriedades do controle de fonte</span><span class="sxs-lookup"><span data-stu-id="da9ac-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="da9ac-118">**\_FONTDELTASIZE da interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="da9ac-118">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="da9ac-119">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="da9ac-119">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 