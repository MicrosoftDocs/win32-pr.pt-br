---
description: Os tipos de contador não de computação não têm uma fórmula associada. O valor bruto é diretamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipos de contador não de computação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a05da34058ceeb99ab60d8cc3d4f72cb3eec85194e48bb707a929eb2f68aa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555156"
---
# <a name="noncomputational-counter-types"></a>Tipos de contador não de computação

Os tipos de contador não de computação não têm uma fórmula associada. O valor bruto é diretamente significativo.

A **propriedade FilesToBeIndexed** na classe [**Win32 \_ PerfRawData \_ ContentIndex \_ IndexingService**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) é um exemplo do tipo de contador **PERF COUNTER \_ \_ RAWCOUNT.** Ele contém uma contagem de arquivos que não foram indexados.

Os tipos de contador são designados pela constante definida no Winperf.h localizada no SDK (Software Development Kit) do Microsoft Windows. A tabela a seguir lista os tipos de contadores não organizacionais fornecidos.



| Countertype                                                                                                 | Descrição                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ COUNTER \_ TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816<br/>                | Esse tipo de contador mostra uma cadeia de caracteres de texto de comprimento variável em Unicode. Ele não exibe valores calculados.               |
| [PERF \_ COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536<br/>           | Valor bruto do contador que não exige cálculos e representa uma amostra que é apenas o último valor observado. |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | O mesmo **que PERF \_ COUNTER \_ RAWCOUNT**, mas uma representação de 64 bits para valores maiores.                                    |
| [PERF \_ COUNTER \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Valor observado mais recentemente em formato hexadecimal. Ele não exibe uma média.                                    |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256<br/> | O mesmo **que PERF \_ COUNTER \_ RAWCOUNT \_ HEX**, mas uma representação de 64 bits em hexadecimal para uso com valores grandes.        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de contador de desempenho WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

