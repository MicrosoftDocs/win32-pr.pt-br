---
description: O atributo swapinputs especifica se as entradas de transição devem ser trocadas. Se o valor for TRUE, as entradas serão trocadas. O valor padrão é FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Atributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b74d16d9b195f504188f4684cf234a5b0c7627274c6e74d57e6824df20a0c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951705"
---
# <a name="swapinputs-attribute"></a>Atributo swapinputs

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `swapinputs` atributo especifica se as entradas de transição devem ser trocadas. Se o valor for **true**, as entradas serão trocadas. O valor padrão é **FALSE**.

## <a name="possible-values"></a>Valores possíveis

Os valores a seguir são definidos como TRUE: y, Y, t, T, 1. Os valores a seguir são definidos como FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Aplica-se A

[**transição**](transition-element.md)

## <a name="remarks"></a>Comentários

Por padrão, uma transição prossegue da composição de todas as camadas de prioridade inferior para a camada na qual reside a transição. Se o `swapinputs` atributo for 1, essa direção será invertida. Para obter mais informações sobre o modelo de camadas usado pelo DES, consulte [o modelo de linha do tempo](the-timeline-model.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



