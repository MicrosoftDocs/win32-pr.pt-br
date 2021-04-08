---
description: O atributo mLength especifica a duração de um arquivo de origem. Esse valor deve ser a duração real ou erros de renderização podem ocorrer.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Atributo mLength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919677"
---
# <a name="mlength-attribute"></a>Atributo mLength

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `mlength` atributo especifica a duração de um arquivo de origem. Esse valor deve ser a duração real ou erros de renderização podem ocorrer.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos. Exemplo: 1:04:30.512. As unidades à esquerda podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



