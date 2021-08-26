---
description: O atributo mlength especifica a duração de um arquivo de origem. Esse valor deve ser a duração real ou podem ocorrer erros de renderização.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Atributo mlength
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2aac65cd917fe99e296298bac425e0ff76ca18fc51c82e9294eaedf0ef1c23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051146"
---
# <a name="mlength-attribute"></a>Atributo mlength

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `mlength` atributo especifica a duração de um arquivo de origem. Esse valor deve ser a duração real ou podem ocorrer erros de renderização.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh:mm:ss.ff,* em que *hh* = horas, *mm* = minutos, *ss* = segundos e *ff* = frações de segundos. Exemplo: 1:04:30.512. As unidades à frente podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



