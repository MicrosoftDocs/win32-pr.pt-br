---
description: O atributo time especifica a hora em que um parâmetro assume um novo valor, em relação ao início da transição ou efeito.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Atributo de tempo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172189"
---
# <a name="time-attribute"></a>Atributo de tempo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `time` atributo especifica a hora em que um parâmetro assume um novo valor, em relação ao início da transição ou efeito.

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos. Exemplo: 1:04:30.512. As unidades à esquerda podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="applies-to"></a>Aplica-se A

[**em**](at-element.md), [ **linear**](linear-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> </dl>

 

 



