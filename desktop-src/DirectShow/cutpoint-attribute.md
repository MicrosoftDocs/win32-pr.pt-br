---
description: O atributo cutpoint especifica quando uma transição corta de uma origem para a próxima, se a transição for renderizada como um recorte. O valor é relativo ao início da transição.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Atributo cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087631"
---
# <a name="cutpoint-attribute"></a>Atributo cutpoint

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `cutpoint` atributo especifica quando uma transição corta de uma origem para a próxima, se a transição for renderizada como um recorte. O valor é relativo ao início da transição.

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos. Exemplo: 1:04:30.512. As unidades à esquerda podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="applies-to"></a>Aplica-se A

[**transição**](transition-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



