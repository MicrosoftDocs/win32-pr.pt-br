---
description: O tipo \_ de dados REFERENCE TIME define as unidades para tempos de referência em DirectShow. Cada unidade de tempo de referência é de 100 nanossegundos.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f1600e820ac59c53144743933701a61e4a7b753f814dde06c5c663a760938d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747316"
---
# <a name="reference_time"></a>TEMPO \_ DE REFERÊNCIA

O **tipo de dados REFERENCE \_ TIME** define as unidades para tempos de referência em DirectShow. Cada unidade de tempo de referência é de 100 nanossegundos.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Comentários

O **tipo de dados REFERENCE \_ TIME** é um inteiro de 64 bits.

Os tempos de referência geralmente são medidos de uma das seguintes linhas de base:

-   Uma hora de relógio absoluta. Nesse caso, a linha de base dependerá da implementação do relógio. Para obter mais informações, consulte [Relógios de referência.](reference-clocks.md)
-   Em relação ao início da reprodução.

Para obter mais informações sobre tempos de referência, consulte [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Strmif.h (inclua Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Tipos de dados](directshow-data-types.md)
</dt> </dl>

 

 




