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
# <a name="aria-range-control-attributes-incompatible"></a>Atributos de controle de intervalo do ARIA incompatíveis

## <a name="text"></a>Texto

O elemento tem a função **ProgressBar** ou **Slider** , mas o valor do **aria-valuenow** exposto está fora do intervalo Aria **-valuemin** do **Aria-VALUEMAX** .

## <a name="type"></a>Tipo

Erro

## <a name="description"></a>Descrição

Esse erro se aplica a elementos que têm uma [**função**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícita ou explícita) igual a **ProgressBar**, **Slider** ou **SpinButton**.

Esse erro indica que o valor de [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) exposto não está no intervalo definido pelos atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Para corrigir esse erro, verifique sua implementação para garantir que os atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) e [**Aria-VALUEMAX**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) estejam definidos corretamente e que o valor do atributo [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) seja mantido corretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de controle de intervalo do ARIA ausentes](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




