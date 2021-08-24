---
title: Atributos de controle de intervalo do ARIA ausentes
description: Atributos de controle de intervalo do ARIA ausentes
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44e4e5c69ea6971846ed9ef5f3a6108bb488c6effb21a6cbc75953ed1bb780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645111"
---
# <a name="aria-range-control-attributes-missing"></a>Atributos de controle de intervalo do ARIA ausentes

## <a name="text"></a>Texto

O elemento tem  **função de** barra de progresso ou controle deslizante, mas não expõe atributos **aria-valuemin** correspondentes, **aria-valuemax** e **aria-valuenow.**

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos que têm uma [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícita ou explícita) igual à barra de **progresso,** controle deslizante ou **spinbutton**.

De acordo com a especificação Iniciativa de Acessibilidade da Web – Aplicativos de Internet Rich Internet Acessíveis (GUID-ARIA), os elementos que têm a função **progressbar**, **controle** deslizante ou **spinbutton** devem expor os atributos [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)

Para corrigir esse erro, de definir os atributos [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)e [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e manter dinamicamente o valor **aria-valuenow** para garantir que o valor atual seja exposto. Você também deve definir o [**atributo aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para adicionar mais significado ao valor **aria-valuenow** exposto.

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

[Atributos de controle de intervalo ARIA incompatíveis](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




