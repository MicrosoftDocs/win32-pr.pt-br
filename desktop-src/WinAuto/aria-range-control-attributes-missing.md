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
# <a name="aria-range-control-attributes-missing"></a>Atributos de controle de intervalo do ARIA ausentes

## <a name="text"></a>Texto

O elemento tem a função **ProgressBar** ou **Slider** , mas não está expondo os atributos correspondentes do **Aria-valuemin** , **Aria-VALUEMAX** e **aria-valuenow** .

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos que têm uma [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícita ou explícita) que é igual a **ProgressBar**, **Slider** ou **SpinButton**.

De acordo com a especificação do WAI-ARIA (aplicativos de Internet sofisticados) acessíveis, os elementos que têm a função **ProgressBar**, **Slider** ou **SpinButton** devem expor os atributos [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Para corrigir esse erro, defina os atributos [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e mantenha o valor do **aria-valuenow** dinamicamente para garantir que o valor atual seja exposto. Você também deve definir o atributo [**Aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para adicionar mais significado ao valor de **aria-valuenow** exposto.

## <a name="example"></a>Exemplo


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de controle de intervalo do ARIA incompatíveis](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




