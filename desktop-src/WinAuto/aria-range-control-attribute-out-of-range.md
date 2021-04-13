---
title: Atributos de controle de intervalo do ARIA incompatíveis
description: Atributos de controle de intervalo do ARIA incompatíveis
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104499178"
---
# <a name="aria-range-control-attributes-incompatible"></a><span data-ttu-id="00ab3-104">Atributos de controle de intervalo do ARIA incompatíveis</span><span class="sxs-lookup"><span data-stu-id="00ab3-104">ARIA Range Control Attributes Incompatible</span></span>

## <a name="text"></a><span data-ttu-id="00ab3-105">Texto</span><span class="sxs-lookup"><span data-stu-id="00ab3-105">Text</span></span>

<span data-ttu-id="00ab3-106">O elemento tem a função **ProgressBar** ou **Slider** , mas o valor do **aria-valuenow** exposto está fora do intervalo Aria **-valuemin** do **Aria-VALUEMAX** .</span><span class="sxs-lookup"><span data-stu-id="00ab3-106">Element has **progressbar** or **slider** role but exposed **aria-valuenow** value is outside of **aria-valuemin** **aria-valuemax** range.</span></span>

## <a name="type"></a><span data-ttu-id="00ab3-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="00ab3-107">Type</span></span>

<span data-ttu-id="00ab3-108">Erro</span><span class="sxs-lookup"><span data-stu-id="00ab3-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="00ab3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="00ab3-109">Description</span></span>

<span data-ttu-id="00ab3-110">Esse erro se aplica a elementos que têm uma [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícita ou explícita) igual a **ProgressBar**, **Slider** ou **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="00ab3-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="00ab3-111">Esse erro indica que o valor de [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) exposto não está no intervalo definido pelos atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="00ab3-111">This error indicates that the exposed [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) value is not in the range defined by the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="00ab3-112">Para corrigir esse erro, verifique sua implementação para garantir que os atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) estejam definidos corretamente e que o valor do atributo [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) seja mantido corretamente.</span><span class="sxs-lookup"><span data-stu-id="00ab3-112">To fix this error, check your implementation to ensure that the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes are correctly set, and that the [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute value is properly maintained.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00ab3-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="00ab3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00ab3-114">Atributos de controle de intervalo do ARIA ausentes</span><span class="sxs-lookup"><span data-stu-id="00ab3-114">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




