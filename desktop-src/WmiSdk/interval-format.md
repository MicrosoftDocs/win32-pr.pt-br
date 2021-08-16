---
description: Define intervalos de data e hora com um formato semelhante à sintaxe de data e hora, quebrando a cadeia de caracteres nos campos por dias, horas, minutos, segundos e microssegundos.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato de intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30db455b6b39349b3da2f8328b22597d8b9c16c47387ba7f6b15d81e62ceb134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318532"
---
# <a name="interval-format"></a>Formato de intervalo

O WMI define intervalos de data e hora com um formato semelhante à sintaxe de data e hora, quebrando a cadeia de caracteres nos campos por dias, horas, minutos, segundos e microssegundos.

O exemplo a seguir mostra o formato de um intervalo de data e hora.

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

A tabela a seguir lista os campos do intervalo de data e hora.



| Campo    | Descrição                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dddddddd | Oito dígitos que representam um número de dias (000000000 a 99999999).                                                                                                                                                                    |
| HH       | Hora de dois dígitos do dia que usa o relógio de 24 horas (00 a 23).                                                                                                                                                                       |
| MM       | Minuto de dois dígitos na hora (00 a 59).                                                                                                                                                                                                |
| SS       | Número de dois dígitos de segundos no minuto (00 a 59).                                                                                                                                                                                   |
| Mmmmmm   | Número de seis dígitos de microssegundos no segundo (000000 a 999999). Sua implementação não é necessária para dar suporte à avaliação usando esse campo, mas esse campo sempre deve estar presente para preservar a natureza de comprimento fixo da cadeia de caracteres. |



 

Os intervalos sempre têm um ":000" à parte final como os últimos quatro caracteres. Além disso, ao contrário da data e hora, você não pode usar asteriscos para indicar campos não usado. Além disso, todas as propriedades do tipo [CIM \_ DATETIME](cim-datetime.md) que representam intervalos devem ser marcadas com o qualificador padrão [SubType,](standard-wmi-qualifiers.md) com o qualificador definido como "interval".

A cadeia de caracteres a seguir representa um intervalo de 1 dia, 12 horas, 0 minutos e 32 segundos.

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de data e hora](date-and-time-format.md)
</dt> <dt>

[Sobre o WMI](about-wmi.md)
</dt> <dt>

[CIM \_ DATETIME](cim-datetime.md)
</dt> </dl>

 

 



