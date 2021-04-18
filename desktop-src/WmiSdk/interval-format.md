---
description: Define os intervalos de data e hora com um formato semelhante à sintaxe de data e hora, dividindo a cadeia de caracteres nos campos de dias, horas, minutos, segundos e microssegundos.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato do intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750090"
---
# <a name="interval-format"></a>Formato do intervalo

O WMI define os intervalos de data e hora com um formato semelhante à sintaxe de data e hora, dividindo a cadeia de caracteres nos campos de dias, horas, minutos, segundos e microssegundos.

O exemplo a seguir mostra o formato de um intervalo de data e hora.

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

A tabela a seguir lista os campos do intervalo de data e hora.



| Campo    | Descrição                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dddddddd | Oito dígitos que representam um número de dias (00000000 a 99999999).                                                                                                                                                                    |
| HH       | A hora de dois dígitos do dia que usa o relógio de 24 horas (00 a 23).                                                                                                                                                                       |
| MM       | Minuto de dois dígitos na hora (00 a 59).                                                                                                                                                                                                |
| SS       | Número de segundos de dois dígitos no minuto (00 a 59).                                                                                                                                                                                   |
| mmmmmm   | Número de seis dígitos de microssegundos no segundo (000000 a 999999). Sua implementação não é necessária para dar suporte à avaliação usando esse campo, mas esse campo sempre deve estar presente para preservar a natureza de comprimento fixo da cadeia de caracteres. |



 

Os intervalos sempre têm um ": 000" à direita como os últimos quatro caracteres. Além disso, diferentemente da data e hora, você não pode usar asteriscos para indicar campos não utilizados. Além disso, todas as propriedades do [tipo \_ data e hora CIM](cim-datetime.md) que representam intervalos devem ser marcadas com o qualificador padrão de [subtipo](standard-wmi-qualifiers.md) , com o qualificador definido como "Interval".

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

[\_data e hora CIM](cim-datetime.md)
</dt> </dl>

 

 



