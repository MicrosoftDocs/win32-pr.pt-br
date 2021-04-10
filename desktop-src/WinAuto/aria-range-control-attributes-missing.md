---
title: Atributos de controle de intervalo do ARIA ausentes
description: Atributos de controle de intervalo do ARIA ausentes
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104008533"
---
# <a name="aria-range-control-attributes-missing"></a><span data-ttu-id="c36d4-104">Atributos de controle de intervalo do ARIA ausentes</span><span class="sxs-lookup"><span data-stu-id="c36d4-104">ARIA Range Control Attributes Missing</span></span>

## <a name="text"></a><span data-ttu-id="c36d4-105">Texto</span><span class="sxs-lookup"><span data-stu-id="c36d4-105">Text</span></span>

<span data-ttu-id="c36d4-106">O elemento tem a função **ProgressBar** ou **Slider** , mas não está expondo os atributos correspondentes do **Aria-valuemin** , **Aria-VALUEMAX** e **aria-valuenow** .</span><span class="sxs-lookup"><span data-stu-id="c36d4-106">Element has **progressbar** or **slider** role but is not exposing corresponding **aria-valuemin** , **aria-valuemax** , and **aria-valuenow** attributes.</span></span>

## <a name="type"></a><span data-ttu-id="c36d4-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c36d4-107">Type</span></span>

<span data-ttu-id="c36d4-108">Erro</span><span class="sxs-lookup"><span data-stu-id="c36d4-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="c36d4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c36d4-109">Description</span></span>

<span data-ttu-id="c36d4-110">Esse erro se aplica a elementos que têm uma [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícita ou explícita) que é igual a **ProgressBar**, **Slider** ou **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="c36d4-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) that is equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="c36d4-111">De acordo com a especificação do WAI-ARIA (aplicativos de Internet sofisticados) acessíveis, os elementos que têm a função **ProgressBar**, **Slider** ou **SpinButton** devem expor os atributos [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="c36d4-111">According to the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) specification, elements that have the **progressbar**, **slider**, or **spinbutton** role must expose the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="c36d4-112">Para corrigir esse erro, defina os atributos [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e mantenha o valor do **aria-valuenow** dinamicamente para garantir que o valor atual seja exposto.</span><span class="sxs-lookup"><span data-stu-id="c36d4-112">To fix this error, set the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes, and dynamically maintain the **aria-valuenow** value to ensure that the current value is exposed.</span></span> <span data-ttu-id="c36d4-113">Você também deve definir o atributo [**Aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para adicionar mais significado ao valor de **aria-valuenow** exposto.</span><span class="sxs-lookup"><span data-stu-id="c36d4-113">You should also set the [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to add more meaning to the exposed **aria-valuenow** value.</span></span>

## <a name="example"></a><span data-ttu-id="c36d4-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c36d4-114">Example</span></span>


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a><span data-ttu-id="c36d4-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c36d4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c36d4-116">Atributos de controle de intervalo do ARIA incompatíveis</span><span class="sxs-lookup"><span data-stu-id="c36d4-116">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




