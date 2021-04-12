---
description: Algumas fórmulas exigem uma propriedade de contador e uma propriedade base.
ms.assetid: c14be351-e712-40bd-bab7-5b9ef6cd8a00
ms.tgt_platform: multiple
title: Tipos de contador base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e481fbf093245813d0ce0de2b5f7906316c2378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171094"
---
# <a name="base-counter-types"></a>Tipos de contador base

Algumas fórmulas exigem uma propriedade de contador e uma propriedade base. O valor de base é o denominador na fórmula para o tipo de contador. Em classes de [contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) de dados brutos derivadas do [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), a propriedade base deve seguir imediatamente a propriedade Counter. A propriedade base deve ter o mesmo nome que o contador anterior, com a **\_ base** acrescentada.

Por exemplo, a propriedade **AvgDiskBytesPerRead** no [**Win32 \_ PerfRawData \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) contém o valor bruto, em bytes, transferido do disco durante operações de leitura. Ele tem uma propriedade base, **AvgDiskBytesPerRead \_ base**, que representa o número acumulado de operações. Quando o WMI aplica a fórmula para o tipo de contador especificado, **\_ \_ base média de desempenho**, **AvgDiskBytesPerRead** é dividido por **AvgDiskBytesPerRead \_ base** para produzir o valor médio. Esse valor aparece no monitor do sistema e é armazenado na propriedade [**de \_ LogicalDisk do PerfFormattedData do \_ getfdisk \_ do Win32**](./retrieving-raw-and-formatted-performance-data.md) correspondente. As propriedades de base são usadas somente em classes de dados brutos.

Em classes derivadas do [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), o qualificador do **contador** especifica a propriedade do numerador na classe RAW e o qualificador **base** especifica a propriedade base do denominador.

A tabela a seguir lista os valores constantes de **tipo "MyType** ".



| Constante de tipo                                                                                      | Descrição                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Desempenho \_ Decimal \_ base média](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939458<br/>        | Valor de base usado para calcular **o \_ \_ timer de desempenho médio** e os tipos de contador de **\_ média \_ em massa de desempenho** .                                                                                             |
| [Desempenho \_ CONTADOR \_ de \_ base múltiplo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 1107494144<br/> | Valor base usado para calcular os tipos de contador contador de desempenho múltiplo de temporizador de **\_ contador \_ \_ \_** de perf, **perf \_ 100NSEC \_ multi \_** timer e **perf \_ 100NSEC \_ multi \_ timer \_ inv** . **\_ \_ \_** |
| [Desempenho \_ Decimal \_ de \_ base bruta grande](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939712<br/>     | Valor base encontrado no cálculo da **\_ \_ fração bruta perf**, 64 bits.                                                                                                                         |
| [Desempenho \_ \_Base bruta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 1073939459<br/>            | Valor base usado para calcular o tipo de contador de **\_ \_ fração bruta perf** .                                                                                                                           |
| [Desempenho \_ Decimal de \_ base de exemplo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))1073939457<br/>         | Valor base usado para calcular o **\_ \_ contador de exemplo perf** e os tipos de contador de **\_ \_ fração de exemplo de perf** .                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> <dt>

[Tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))
</dt> </dl>

 

