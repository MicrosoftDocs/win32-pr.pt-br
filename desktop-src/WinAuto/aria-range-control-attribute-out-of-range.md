---
title: Atributos de controle de intervalo do ARIA incompatíveis
description: Atributos de controle de intervalo do ARIA incompatíveis
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f5de18be88682046cac6c4d4156f48fd3e4994d2e7b9ab1bbdc52f0a2e768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326739"
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

 

 




