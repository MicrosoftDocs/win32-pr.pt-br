---
description: O tipo de dados de tempo de referência \_ define as unidades para os tempos de referência no DirectShow. Cada unidade de tempo de referência é de 100 nanossegundos.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812972"
---
# <a name="reference_time"></a>hora de referência \_

O tipo de dados de **\_ tempo de referência** define as unidades para os tempos de referência no DirectShow. Cada unidade de tempo de referência é de 100 nanossegundos.


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>Comentários

O tipo de dados de **\_ tempo de referência** é um inteiro de 64 bits.

Os tempos de referência geralmente são medidos a partir de uma das seguintes linhas de base:

-   Um tempo de relógio absoluto. Nesse caso, a linha de base dependerá da implementação do relógio. Para obter mais informações, consulte [relógios de referência](reference-clocks.md).
-   Em relação ao início da reprodução.

Para obter mais informações sobre os tempos de referência, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Strmif. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados do DirectShow](directshow-data-types.md)
</dt> </dl>

 

 




