---
description: Representam diferenças entre amostras ao longo do tempo e geralmente usa um valor base para o cálculo.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Tipos de contador de algoritmos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797632"
---
# <a name="basic-algorithm-counter-types"></a>Tipos de contador de algoritmos básicos

Os tipos de contador de algoritmos básicos geralmente representam as diferenças entre os exemplos ao longo do tempo e geralmente usam um valor base para o cálculo. Por exemplo, a propriedade **PercentFreeSpace** da classe [**de \_ PhysicalDisk do PerfFormattedData de \_ perfdisk \_ do Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) representa a proporção do espaço livre disponível na unidade de disco físico para o espaço utilizável total fornecido pela unidade de disco físico selecionada. Essa classe também contém o valor base, **PercentFreeSpace \_ base**. A porcentagem de espaço livre em disco é obtida com a divisão de **PercentFreeSpace** por **PercentFreeSpace \_ base** e a multiplicação por 100%.

Os algoritmos básicos na tabela a seguir são fornecidos.



| Constante de tipo                                                                                    | Descrição                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Desempenho \_ \_Fração bruta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 537003008<br/>       | Taxa de um subconjunto para seu conjunto como uma porcentagem. Esse tipo de contador exibe apenas a porcentagem atual, não uma média ao longo do tempo.                                    |
| [Desempenho \_ \_Fração de exemplo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 549585920<br/>    | Taxa média de ocorrências para todas as operações durante os dois últimos intervalos de exemplo. Esse tipo de contador requer uma propriedade base com o \_ tipo de contador de base perf Sample \_ . |
| [Desempenho \_ \_Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal do contador 4195328<br/>        | Esse tipo de contador mostra a alteração no atributo medido entre os dois intervalos de amostra mais recentes.                                                         |
| [Desempenho \_ Decimal \_ \_ Delta grande do contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))4195584<br/> | O mesmo que \_ o Delta do contador de desempenho \_ , mas uma representação de 64 bits para valores maiores.                                                                                        |
| [Desempenho \_ \_Tempo decorrido](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 807666944<br/>       | Tempo total entre o início do processo e a hora em que esse valor é calculado.                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

